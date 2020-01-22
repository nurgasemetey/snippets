###  swagger configuration in spring boot


[Setting Up Swagger 2 with a Spring REST API | Baeldung](https://www.baeldung.com/swagger-2-documentation-for-spring-rest-api "Setting Up Swagger 2 with a Spring REST API | Baeldung")


 

```java
@Configuration
@EnableSwagger2
public class SpringFoxConfig {
    static Set<String> DEFAULT_PRODUCES_AND_CONSUMES = new HashSet<String>(Arrays.asList("application/json"));
    @Bean
    public Docket api() { 
        return new Docket(DocumentationType.SWAGGER_2)
                .apiInfo(new ApiInfoBuilder()
                        .title("Internal Control App API")
                        .termsOfServiceUrl("https://paraboly.com")
                        .version("1.0.0")
                        .build())
                .produces(DEFAULT_PRODUCES_AND_CONSUMES)
                .consumes(DEFAULT_PRODUCES_AND_CONSUMES)
                .select()
                .apis(RequestHandlerSelectors.basePackage("com.parabol.kgmmicroservices"))
                .paths(PathSelectors.any())
                .build();
    }
}
```
