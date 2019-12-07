###  Run minio from cli





 

```shell
docker run -p 9000:9000 -e PORT=9000 -e MINIO_ACCESS_KEY=parabol2011 -e MINIO_SECRET_KEY=parabol2011 -it minio/minio server /data
```
