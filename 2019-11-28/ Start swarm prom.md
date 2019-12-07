###  Start swarm prom





 

```shell
ADMIN_USER=admin \
ADMIN_PASSWORD=admin \
SLACK_URL=https://hooks.slack.com/services/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 \
SLACK_CHANNEL=devops-alerts \
SLACK_USER=devops-alerts \
docker stack deploy -c docker-compose.yml mon
```

