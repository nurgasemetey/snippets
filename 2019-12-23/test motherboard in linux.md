### test motherboard in linux


[ubuntu - How do I test if my motherboard is failing using Linux? - Super User](https://superuser.com/questions/682344/how-do-i-test-if-my-motherboard-is-failing-using-linux)

```shell
sudo dmidecode |grep -B 2 Stat
```

