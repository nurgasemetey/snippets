### Nginx docker run example







```shell
docker run --name docker-nginx -p 80:80  -v /home/issd/text-engine-master:/usr/share/nginx/html -v /home/issd/nginx/default.conf:/etc/nginx/conf.d/default.conf -d nginx
```
