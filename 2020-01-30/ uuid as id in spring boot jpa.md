###  uuid as id in spring boot jpa


[Spring Boot with PostgreSQL, Flyway, and JSONB | Okta Developer](https://developer.okta.com/blog/2019/02/20/spring-boot-with-postgresql-flyway-jsonb "Spring Boot with PostgreSQL, Flyway, and JSONB | Okta Developer")



[java - Spring Data cannot fetch a record using UUID in postgresql - Stack Overflow](https://stackoverflow.com/questions/49688308/spring-data-cannot-fetch-a-record-using-uuid-in-postgresql "java - Spring Data cannot fetch a record using UUID in postgresql - Stack Overflow")


 

```java
    @Id @Type(type="org.hibernate.type.UUIDCharType") @GeneratedValue
    private UUID id;

```
