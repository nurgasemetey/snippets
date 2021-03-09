### docker swarm restart service


[Restart one service in docker swarm stack - Stack Overflow](https://stackoverflow.com/questions/44811886/restart-one-service-in-docker-swarm-stack "Restart one service in docker swarm stack - Stack Overflow")


 

```
$ docker stack services <stack_name>
ID                  NAME              ...
3xrdy2c7pfm3        stack-name_api    ...

$ docker service update --force 3xrdy2c7pfm3
```
