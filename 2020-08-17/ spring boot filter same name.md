###  spring boot filter same name


[java - How to add a filter class in Spring Boot? - Stack Overflow](https://stackoverflow.com/questions/19825946/how-to-add-a-filter-class-in-spring-boot "java - How to add a filter class in Spring Boot? - Stack Overflow")


 

```
One important thing to note is that the name of your bean (based on your class name) should not be the same as a Spring bean. For instance, you might be tempted to create a MetricsFilter, but this bean will be overshadowed by the Spring actuator bean of the same name. Learned this the hard way...
```
