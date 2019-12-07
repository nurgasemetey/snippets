###  Find name of process by its pid, process number


[linux - If I know the PID number of a process, how can I get its name? - Super User](https://superuser.com/questions/632979/if-i-know-the-pid-number-of-a-process-how-can-i-get-its-name "linux - If I know the PID number of a process, how can I get its name? - Super User")


 

```shell
cat /proc/pid/cmdline

```
