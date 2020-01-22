### spring boot jpa lombok entity example


[Integrating Spring Data JPA, PostgreSQL, and Liquibase](https://auth0.com/blog/integrating-spring-data-jpa-postgresql-liquibase/ "Integrating Spring Data JPA, PostgreSQL, and Liquibase")


 

```java
@Entity
@Data
public class InternalControl {
    private static final long serialVersionUID = -2343243243242432341L;
    @Id
    @GeneratedValue(strategy = GenerationType.AUTO)
    private Long id;

    @CreatedDate
    private Date createdAt;

    @LastModifiedDate
    private Date updatedAt;
    @NotNull
    private String biddingNo;
    @NotNull
    private int biddingNoYear;
    @NotNull
    private int biddingNoText;
```
