###  unique value column spring data jpa


[Spring Data JPA - Get All Unique Values in Column - Stack Overflow](https://stackoverflow.com/questions/42619129/spring-data-jpa-get-all-unique-values-in-column "Spring Data JPA - Get All Unique Values in Column - Stack Overflow")


 

```java
  @Query("SELECT DISTINCT a.city FROM Address a")
  List<String> findDistinctCity();
```
