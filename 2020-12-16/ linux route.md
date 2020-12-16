###  linux route


[networking - How to set static routes in Ubuntu Server? - Ask Ubuntu](https://askubuntu.com/questions/168033/how-to-set-static-routes-in-ubuntu-server "networking - How to set static routes in Ubuntu Server? - Ask Ubuntu")


 

```
up route add -net {someip} netmask 255.255.255.0 gw {gateway}
```
