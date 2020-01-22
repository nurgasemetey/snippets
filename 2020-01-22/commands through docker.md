### commands through docker


[linux - Trying to run chmod inside docker container in a single command - Stack Overflow](https://stackoverflow.com/questions/50394706/trying-to-run-chmod-inside-docker-container-in-a-single-command "linux - Trying to run chmod inside docker container in a single command - Stack Overflow")




```shell
docker exec  openproject bash -c "chown -R postgres:postgres /var/openproject/pgdata"
docker exec  openproject bash -c "chmod 700 -R /var/openproject/pgdata"
docker exec  openproject bash -c "ls -la /var/openproject/pgdata"

```
