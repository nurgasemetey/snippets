### List containers from all nodes of docker swarm mode


[List containers from all nodes of docker swarm mode - Server Fault](https://serverfault.com/questions/857758/list-containers-from-all-nodes-of-docker-swarm-mode "List containers from all nodes of docker swarm mode - Server Fault")


 

```shell
docker node ps $(docker node ls -q)
```
