###  spring boot 2 disable endpoints


[Spring Boot Actuator: Production-ready Features](https://docs.spring.io/spring-boot/docs/current/reference/html/production-ready-features.html#production-ready-kubernetes-probes "Spring Boot Actuator: Production-ready Features")


 

```
//remove from pom.xml
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-actuator</artifactId>
    </dependency>
</dependencies>

//if you want disable all but enable some of
management.endpoints.enabled-by-default=false
```
