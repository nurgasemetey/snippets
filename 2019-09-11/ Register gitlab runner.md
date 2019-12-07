###  Register gitlab runner





 

```shell
sudo gitlab-runner register -n \
   --url https://gitlab.com/ \
   --registration-token FZHjdzW99UR5sv4PV4-P\
   --executor shell \
   --env='PROFILE=docker-compose.swarm-test.yml'\
   --tag-list "test" \
   --description "Test Server"
```
