###  Configure hikari in spring boot


[spring.datasource.hikari.maxLifetime=2000000](https://stackoverflow.com/questions/54779350/spring-jpa-with-hikari-not-releasing-connection "postgresql - Spring JPA with Hikari not releasing connection - Stack Overflow")



[Configuring a Hikari Connection Pool with Spring Boot | Baeldung](https://www.baeldung.com/spring-boot-hikari "Configuring a Hikari Connection Pool with Spring Boot | Baeldung")


 

```shell
spring.datasource.hikari.minimumIdle=5
spring.datasource.hikari.maximumPoolSize=20
spring.datasource.hikari.idleTimeout=30000
spring.datasource.hikari.poolName=SpringBootJPAHikariCP
spring.datasource.hikari.maxLifetime=2000000
spring.datasource.hikari.testWhileIdle=true
spring.datasource.hikari.validationQuery=SELECT 1
spring.datasource.hikari.connectionTimeout=30000 


```
