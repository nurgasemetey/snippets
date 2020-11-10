###  spring boot conditional component property


[Conditional Beans with Spring Boot](https://reflectoring.io/spring-boot-conditionals/ "Conditional Beans with Spring Boot")


 

```
@Configuration
@ConditionalOnProperty(
    value="module.enabled", 
    havingValue = "true", 
    matchIfMissing = true)
class CrossCuttingConcernModule {
  ...
}
```
