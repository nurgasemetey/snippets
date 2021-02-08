### docker redis run password


[How do I set a password for redis? · Issue #176 · docker-library/redis](https://github.com/docker-library/redis/issues/176 "How do I set a password for redis? · Issue #176 · docker-library/redis")


 

```
docker run --name redis -d -p 6379:6379 redis redis-server --requirepass "SUPER_SECRET_PASSWORD"
```
