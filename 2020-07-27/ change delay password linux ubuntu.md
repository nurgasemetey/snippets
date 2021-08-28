###  change delay password linux ubuntu


[How can I lower the delay after incorrectly entered login and sudo passwords? - Ask Ubuntu](https://askubuntu.com/questions/877385/how-can-i-lower-the-delay-after-incorrectly-entered-login-and-sudo-passwords "How can I lower the delay after incorrectly entered login and sudo passwords? - Ask Ubuntu")


 

```
Edit /etc/pam.d/common-auth and add nodelay: e.g.:
auth       optional     pam_faildelay.so  delay=500000
```
