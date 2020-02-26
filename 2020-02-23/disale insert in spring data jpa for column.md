### disale insert in spring data jpa for column


[Persist extra attributes for relationships with JPA &amp; Hibernate](https://thoughts-on-java.org/many-relationships-additional-properties/ "Persist extra attributes for relationships with JPA &amp; Hibernate")


 

```java
	@JoinColumn(name = "fk_publisher", insertable = false, updatable = false)

```
