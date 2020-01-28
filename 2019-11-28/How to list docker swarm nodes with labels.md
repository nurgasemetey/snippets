### How to list docker swarm nodes with labels


[How to list docker swarm nodes with labels - Stack Overflow](https://stackoverflow.com/questions/42414703/how-to-list-docker-swarm-nodes-with-labels "How to list docker swarm nodes with labels - Stack Overflow")




```shell
docker node ls -q | xargs docker node inspect   -f '{{ .ID }} [{{ .Description.Hostname }}]: {{ .Spec.Labels }}: {{ .Status.Addr}}'
```
