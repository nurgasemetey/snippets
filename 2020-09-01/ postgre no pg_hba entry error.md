###  postgre no pg_hba entry error


[perl - no pg_hba.conf entry for host - Stack Overflow](https://stackoverflow.com/questions/1406025/no-pg-hba-conf-entry-for-host "perl - no pg_hba.conf entry for host - Stack Overflow")


 

```
no pg_hba.conf entry for host

---
If you can change this line:

host    all        all         192.168.0.1/32        md5
With this:

host    all        all         all                   md5
You can see if this solves the problem.
```
