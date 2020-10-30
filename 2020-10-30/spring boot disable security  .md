### spring boot disable security  


[Disable Security for a Profile in Spring Boot | Baeldung](https://www.baeldung.com/spring-security-disable-profile "Disable Security for a Profile in Spring Boot | Baeldung")


 

```
	@Profile("test")
@Configuration
public class ApplicationSecurity extends WebSecurityConfigurerAdapter {
    @Override
    public void configure(WebSecurity web) throws Exception {
        web.ignoring().antMatchers("/**");
    }
}
```
