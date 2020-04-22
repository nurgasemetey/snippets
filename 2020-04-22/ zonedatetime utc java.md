###  zonedatetime utc java


[datetime - How to get milliseconds from LocalDateTime in Java 8 - Stack Overflow](https://stackoverflow.com/questions/23944370/how-to-get-milliseconds-from-localdatetime-in-java-8 "datetime - How to get milliseconds from LocalDateTime in Java 8 - Stack Overflow")


 

```java
long millis = zdt.toInstant().toEpochMilli();

```
