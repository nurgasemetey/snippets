### spring boot notnull request body 


[Difference Between @NotNull, @NotEmpty, and @NotBlank Constraints in Bean Validation | Baeldung](https://www.baeldung.com/java-bean-validation-not-null-empty-blank "Difference Between @NotNull, @NotEmpty, and @NotBlank Constraints in Bean Validation | Baeldung")


 

```
public class UserNotNull {
    
    @NotNull(message = "Name may not be null")
    private String name;
    
    // standard constructors / getters / toString   
}
```
