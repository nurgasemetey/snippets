###  Spring Boot access static resources


[java - Spring Boot access static resources missing scr/main/resources - Stack Overflow](https://stackoverflow.com/questions/36371748/spring-boot-access-static-resources-missing-scr-main-resources "java - Spring Boot access static resources missing scr/main/resources - Stack Overflow")


 

```java
InputStream is = new ClassPathResource("countries.xml").getInputStream();

```
