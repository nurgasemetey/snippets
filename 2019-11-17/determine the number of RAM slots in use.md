### determine the number of RAM slots in use


[linux - How do I determine the number of RAM slots in use? - Unix &amp; Linux Stack Exchange](https://unix.stackexchange.com/questions/33249/how-do-i-determine-the-number-of-ram-slots-in-use "linux - How do I determine the number of RAM slots in use? - Unix &amp; Linux Stack Exchange")




```shell
dmidecode -t memory
dmidecode -t 16
lshw -class memory
```
