###  file limit spring boot


[java - Max limit of MultipartFile in Spring Boot - Stack Overflow](https://stackoverflow.com/questions/34177873/max-limit-of-multipartfile-in-spring-boot "java - Max limit of MultipartFile in Spring Boot - Stack Overflow")


 

```yml
spring:
 servlet:
    multipart:
      max-file-size: 15MB
      max-request-size: 15MB
```
