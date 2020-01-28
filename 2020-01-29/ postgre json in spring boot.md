###  postgre json in spring boot


[How to map a String JPA property to a JSON column using Hibernate - Vlad Mihalcea](https://vladmihalcea.com/map-string-jpa-property-json-column-hibernate/ "How to map a String JPA property to a JSON column using Hibernate - Vlad Mihalcea")


 

```
@TypeDefs({
        @TypeDef(
                name = "jsonb",
                typeClass = JsonBinaryType.class
        ),
        @TypeDef(
                name = "string-array",
                typeClass = StringArrayType.class
        )
})
public class InvestmentDetail implements Serializable  {
    @Type(type = "jsonb")
    @Column(columnDefinition = "jsonb")
    private Object geometry;
```
