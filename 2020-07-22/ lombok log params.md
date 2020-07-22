###  lombok log params


[Spring Boot Logging with Lombok - @Slf4j Annotation Example](https://howtodoinjava.com/spring-boot2/logging/logging-with-lombok/ "Spring Boot Logging with Lombok - @Slf4j Annotation Example")


 

```java
@Slf4j
@SpringBootApplication
public class Application 
{
    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
         
        log.info("Simple log statement with inputs {}, {} and {}", 1, 2, 3);
    }
}
```
