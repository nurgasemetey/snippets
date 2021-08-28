### ls large number of files





 

```
tl;dr: try "ls -1 -f". It's fast.
This doesn't pass my smell test:

> Putting two and two together I could see that the reason it was taking forever to list the directory was because ls was reading the directory entries file 32K at a time, and the file was 513M. So it would take around 16416 system calls of getdents() to list the directory. That is a lot of calls, especially on a slow virtualized disk.

16,416 system calls is a little inefficient but not that noticeable on human terms. And the author is talking as if each one waits 10 ms for a disk head to move to the correct position. That's not true. The OS and drive both do readahead, and they're both quite effective. I recently tried to improve performance of a long-running sequential read on an otherwise-idle old-fashioned spinning disk by tuning the former ("sudo blockdev --setra 6144 /path/to/device"). I found it made no real difference: "iostat" showed OS-level readahead reduces the number of block operations (as expected) but also that total latency doesn't decrease. It turns out in this scenario the disk's cache is full of the upcoming bytes so those extra operations are super fast anyway.

The real reason "ls" takes a while to print stuff is that by default it will buffer everything before printing anything so that it can sort it and (when stdout is a terminal) place it into appropriately-sized columns. It also (depending on the options you are using) will stat every file, which obviously will dwarf the number of getdents calls and access the inodes (which are more scattered across the filesystem).

"ls -1 -f" disables both those behaviors. It's reasonably fast without changing the buffer size.

    moonfire-nvr@nuc:/media/14tb/sample$ time ls -1f | wc -l
    1042303

    real    0m0.934s
    user    0m0.403s
    sys     0m0.563s
That's on Linux with ext4.

```
