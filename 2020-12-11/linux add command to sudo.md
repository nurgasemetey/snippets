### linux add command to sudo







```
sudo visudo
issd ALL = NOPASSWD: /bin/cp, /bin/rm, /usr/bin/service
jenkins ALL=(ALL) NOPASSWD: ALL
```
