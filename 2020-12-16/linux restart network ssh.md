### linux restart network ssh


[networking - How to successfully restart a network without reboot over SSH? - Ask Ubuntu](https://askubuntu.com/questions/441619/how-to-successfully-restart-a-network-without-reboot-over-ssh "networking - How to successfully restart a network without reboot over SSH? - Ask Ubuntu")




```
sudo ifdown eth0 && sudo ifup eth0
```
