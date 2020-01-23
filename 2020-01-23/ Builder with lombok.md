###  Builder with lombok


[Lombok Builder with Default Value | Baeldung](https://www.baeldung.com/lombok-builder-default-value "Lombok Builder with Default Value | Baeldung")


 

```java
@Builder
@Data
public class InternalControlElastic {
    @Builder.Default
    private String type = "internalcontrol";
    private String id;
    private String text;
    @Builder.Default
    private String entity = "internalcontrol";
}


InternalControlElastic internalControlElastic = InternalControlElastic.builder().id(entityId).text(internalControlStr).build();
```
