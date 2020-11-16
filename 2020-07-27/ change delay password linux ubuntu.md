###  change delay password linux ubuntu


[How can I lower the delay after incorrectly entered login and sudo passwords? - Ask Ubuntu](https://askubuntu.com/questions/877385/how-can-i-lower-the-delay-after-incorrectly-entered-login-and-sudo-passwords "How can I lower the delay after incorrectly entered login and sudo passwords? - Ask Ubuntu")


 

```
/etc/pam.d/login
add before line which contains pam_unix.so nullok_secure
auth       optional     pam_faildelay.so  delay=500000

```
