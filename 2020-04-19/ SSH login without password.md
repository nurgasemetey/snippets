###  SSH login without password


[SSH login without password](http://www.linuxproblem.org/art_9.html "SSH login without password")


 

```
cat .ssh/id_rsa.pub | ssh issd@192.168.1.194 'cat >> .ssh/authorized_keys'
```
