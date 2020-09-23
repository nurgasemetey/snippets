###  spring boot get yaml field value


[java - Spring boot get application base url outside of servlet context - Stack Overflow](https://stackoverflow.com/questions/40401383/spring-boot-get-application-base-url-outside-of-servlet-context "java - Spring boot get application base url outside of servlet context - Stack Overflow")


 

```
@Value("${server.servlet.context-path}")
    String contextPath;
```
