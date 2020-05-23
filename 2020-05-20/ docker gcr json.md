###  docker gcr json


[Authentication methods | Container Registry Documentation](https://cloud.google.com/container-registry/docs/advanced-authentication#gcloud_1 "Authentication methods  |  Container Registry Documentation")


 

```
cat keyfile.json | docker login -u _json_key --password-stdin https://[HOSTNAME]
docker login -u _json_key -p "$(cat keyfile.json)" https://[HOSTNAME]
where [HOSTNAME] is gcr.io, us.gcr.io, eu.gcr.io, or asia.gcr.io.


```
