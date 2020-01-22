### hard reboot over ssh


[&quot;Last resort&quot; Linux terminal command to reboot (over ssh) in case of a kernel bug? - Unix &amp; Linux Stack Exchange](https://unix.stackexchange.com/questions/183095/last-resort-linux-terminal-command-to-reboot-over-ssh-in-case-of-a-kernel-bu "&quot;Last resort&quot; Linux terminal command to reboot (over ssh) in case of a kernel bug? - Unix &amp; Linux Stack Exchange")


 

```shell
To ensure that the system will reboot no matter what, I always do this sequence:

# echo s > /proc/sysrq-trigger
# echo u > /proc/sysrq-trigger
# echo s > /proc/sysrq-trigger
# echo b > /proc/sysrq-trigger
This requests the kernel to do:

emergency sync of the block devices
mount readonly of all filesystems
again a sync
force an immediate boot; you can also use o for poweroff.
```
