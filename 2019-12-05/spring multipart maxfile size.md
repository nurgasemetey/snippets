### spring multipart maxfile size


[java - SpringBoot's @MultipartConfig maxFileSize not taking effect - Stack Overflow](https://stackoverflow.com/questions/36945482/springboots-multipartconfig-maxfilesize-not-taking-effect "java - SpringBoot's @MultipartConfig maxFileSize not taking effect - Stack Overflow")


 

```shell
For setting custom limits for multipart uploads, the below properties are to be used(for a sample size of 30MB):

spring.http.multipart.max-file-size=30MB
spring.http.multipart.max-request-size=30MB
In our company's projects, I found that one of them was on Spring Boot version 1.3.5, so for versions < 1.4 you should use

multipart.max-file-size=30MB
multipart.max-request-size=30MB
```
