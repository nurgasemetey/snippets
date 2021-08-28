### bash multiple line variables write


[linux - How to write multiple line string using Bash with variables? - Stack Overflow](https://stackoverflow.com/questions/7875540/how-to-write-multiple-line-string-using-bash-with-variables "linux - How to write multiple line string using Bash with variables? - Stack Overflow")


 

```
#!/bin/bash

kernel="2.6.39"
distro="xyz"
cat >/etc/myconfig.conf <<EOL
line 1, ${kernel}
line 2, 
line 3, ${distro}
line 4 line
... 
EOL

cat /etc/myconfig.conf
```
