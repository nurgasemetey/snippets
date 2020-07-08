###  java stream sum array list


[Summing Numbers with Java Streams | Baeldung](https://www.baeldung.com/java-stream-sum "Summing Numbers with Java Streams | Baeldung")


 

```java
List<Integer> integers = Arrays.asList(1, 2, 3, 4, 5);
Integer sum = integers.stream()
  .reduce(0, Integer::sum);
```
