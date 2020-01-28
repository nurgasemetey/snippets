###  postgre array in spring boot


[How to map a PostgreSQL Enum ARRAY to a JPA entity property using Hibernate - Vlad Mihalcea](https://vladmihalcea.com/map-postgresql-enum-array-jpa-entity-property-hibernate/ "How to map a PostgreSQL Enum ARRAY to a JPA entity property using Hibernate - Vlad Mihalcea")


 

```java
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

    @Type( type = "string-array" )
    @Column(
            name = "kkn",
            columnDefinition = "text[]"
    )
    private String[] kkn;

```
