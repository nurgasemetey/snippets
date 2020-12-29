### spring boot data jpa batch


[Spring Data JPA Batch Inserts | Baeldung](https://www.baeldung.com/spring-data-jpa-batch-inserts "Spring Data JPA Batch Inserts | Baeldung")



[hibernate - How to do bulk (multi row) inserts with JpaRepository? - Stack Overflow](https://stackoverflow.com/questions/50772230/how-to-do-bulk-multi-row-inserts-with-jparepository "hibernate - How to do bulk (multi row) inserts with JpaRepository? - Stack Overflow")



[java - Spring Data JPA saveAll not doing batch insert - Stack Overflow](https://stackoverflow.com/questions/59002107/spring-data-jpa-saveall-not-doing-batch-insert "java - Spring Data JPA saveAll not doing batch insert - Stack Overflow")


 

```
spring.jpa.properties.hibernate.jdbc.batch_size=50
spring.jpa.properties.hibernate.order_inserts=true
spring.jpa.properties.hibernate.generate_statistics=true
hibernate.order_updates = true


```
