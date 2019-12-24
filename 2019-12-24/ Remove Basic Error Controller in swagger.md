###  Remove Basic Error Controller in swagger


[swagger ui - Remove Basic Error Controller In SpringFox SwaggerUI - Stack Overflow](https://stackoverflow.com/questions/32941917/remove-basic-error-controller-in-springfox-swaggerui)


 

```java
return new Docket(DocumentationType.SWAGGER_2)
                .select()
                .apis(RequestHandlerSelectors.basePackage("com.app.microservice"))
                .build();
```
