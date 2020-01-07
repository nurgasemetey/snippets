### count function in spring data


[java - Does Spring Data JPA have any way to count entites using method name resolving? - Stack Overflow](https://stackoverflow.com/questions/10696490/does-spring-data-jpa-have-any-way-to-count-entites-using-method-name-resolving "java - Does Spring Data JPA have any way to count entites using method name resolving? - Stack Overflow")




```java
public interface UserRepository extends CrudRepository<User, Integer> {
    Long countByName(String name);
}
```
