### Finding the PID of the process using a specific port


[linux - Finding the PID of the process using a specific port? - Unix &amp; Linux Stack Exchange](https://unix.stackexchange.com/questions/106561/finding-the-pid-of-the-process-using-a-specific-port "linux - Finding the PID of the process using a specific port? - Unix &amp; Linux Stack Exchange")


 

```shell
sudo ss -lptn 'sport = :80'
```
