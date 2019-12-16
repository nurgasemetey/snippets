###  directly initialize a HashMap


[java - How to directly initialize a HashMap (in a literal way)? - Stack Overflow](https://stackoverflow.com/questions/6802483/how-to-directly-initialize-a-hashmap-in-a-literal-way "java - How to directly initialize a HashMap (in a literal way)? - Stack Overflow")


 

```java
ap<String, String> test = ImmutableMap.<String, String>builder()
    .put("k1", "v1")
    .put("k2", "v2")
    ...
    .build();
```
