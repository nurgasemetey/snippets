###  spring data optional findbyid


[java - Spring Data JPA findOne() change to Optional how to use this? - Stack Overflow](https://stackoverflow.com/questions/49316751/spring-data-jpa-findone-change-to-optional-how-to-use-this "java - Spring Data JPA findOne() change to Optional how to use this? - Stack Overflow")


 

```java
return repository.findById(id)
        .orElseThrow(() -> new EntityNotFoundException(id));

```
