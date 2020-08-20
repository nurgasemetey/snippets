###  gcloud gcr service account json docker pull


[Authentication methods | Container Registry | Google Cloud](https://cloud.google.com/container-registry/docs/advanced-authentication#json_key_file)


 

```shell
[Configuring access control | Container Registry | Google Cloud](https://cloud.google.com/container-registry/docs/access-control)

Service account for storage admin for pushing and pulling images

cat keyfile.json | docker login -u _json_key --password-stdin https://[HOSTNAME]
where [HOSTNAME] is gcr.io, us.gcr.io, eu.gcr.io, or asia.gcr.io.
```
