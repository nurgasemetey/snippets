### convert class to map


[Java, Convert instance of Class to HashMap - Stack Overflow](https://stackoverflow.com/questions/37024300/java-convert-instance-of-class-to-hashmap "Java, Convert instance of Class to HashMap - Stack Overflow")




```java
MyObject obj = new MyObject();
obj.myInt = 1;
obj.myString = "1";
ObjectMapper mapObject = new ObjectMapper();
Map < String, Object > mapObj = mapObject.convertValue(obj, Map.class);
```
