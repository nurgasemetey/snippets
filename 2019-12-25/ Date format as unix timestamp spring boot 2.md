###  Date format as unix timestamp spring boot 2


[Java json response shows date in numeric value - Stack Overflow](https://stackoverflow.com/questions/52964744/java-json-response-shows-date-in-numeric-value)


 

```shell
If you use Spring boot 2.x instead 1.x ,the default behavior has changed
add spring.jackson.serialization.write-dates-as-timestamps=true to your configuration to return to the previous behavior
Spring Boot 2.0 Migration Guide


```
