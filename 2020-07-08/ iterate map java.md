###  iterate map java


[java - Iterate through a HashMap - Stack Overflow](https://stackoverflow.com/questions/1066589/iterate-through-a-hashmap "java - Iterate through a HashMap - Stack Overflow")


 

```java
Map<String, Object> map = ...;


for (String key : map.keySet()) {
    // ...
}

for (Object value : map.values()) {
    // ...
}

for (Map.Entry<String, Object> entry : map.entrySet()) {
    String key = entry.getKey();
    Object value = entry.getValue();
    // ...
}
```
