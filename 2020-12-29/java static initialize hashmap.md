### java static initialize hashmap


[java - How to directly initialize a HashMap (in a literal way)? - Stack Overflow](https://stackoverflow.com/questions/6802483/how-to-directly-initialize-a-hashmap-in-a-literal-way "java - How to directly initialize a HashMap (in a literal way)? - Stack Overflow")


 

```
Map<String, String> myMap = new HashMap<String, String>() {{
        put("a", "b");
        put("c", "d");
    }};
```
