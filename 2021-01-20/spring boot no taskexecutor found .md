### spring boot no taskexecutor found 


[Investigate the reason of &quot;No TaskExecutor bean found for async processing&quot; message · Issue #472 · php-coder/mystamps](https://github.com/php-coder/mystamps/issues/472 "Investigate the reason of &quot;No TaskExecutor bean found for async processing&quot; message · Issue #472 · php-coder/mystamps")


 

```
Here is the answer https://jira.spring.io/browse/SPR-14271
As Juergen Hoeller noticed - this is INFO-level message, not an ERROR, even not a WARNING.

But he also said "I'd strongly recommend an explicit executor setup indeed". Let's configure executor for async tasks then.

---
@Configuration
@EnableAsync
public class SpringAsyncConfig {

    @Bean
    public TaskExecutor taskExecutor() {
        return new SimpleAsyncTaskExecutor(); // Or use another one of your liking
    }
}
```
