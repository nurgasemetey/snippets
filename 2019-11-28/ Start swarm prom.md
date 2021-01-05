###  Start swarm prom





 

```shell
ADMIN_USER=admin \
ADMIN_PASSWORD=admin \
SLACK_URL=hook url \
SLACK_CHANNEL=devops-alerts \
SLACK_USER=devops-alerts \
docker stack deploy -c docker-compose.yml mon
```

