###  spring data mongo configuration





 

```
In 1.4 Spring Data MongoDB uses Mongo 3 driver:

!!! `spring.data.mongodb.host` and `spring.data.mongodb.port` are not supported if you’re using the Mongo 3.0 Java driver. 

In such case,  `spring.data.mongodb.uri` should be used to provide all of the configuration, like this:

```yaml
spring.data.mongodb.uri=mongodb://metin:12345678@192.168.0.193:27017/iotcentral?authMechanism=SCRAM-SHA-1
```

Just add the `spring.data.mongodb.uri` to your `application.yml` and you'll get the auto configured `MongoDbFactory` and `MongoTemplate`.
```
