### docker default bridge ip address


[How to change the default IP address of docker bridge adapter | Edureka Community](https://www.edureka.co/community/68927/how-to-change-the-default-ip-address-of-docker-bridge-adapter "How to change the default IP address of docker bridge adapter | Edureka Community")


 

```
$ vim /etc/docker/daemon.json
{
  "bip": "172.200.0.1/16"
}
```
