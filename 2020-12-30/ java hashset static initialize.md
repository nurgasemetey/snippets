###  java hashset static initialize


[Initializing HashSet at the Time of Construction | Baeldung](https://www.baeldung.com/java-initialize-hashset "Initializing HashSet at the Time of Construction | Baeldung")


 

```
Set<String> set = new HashSet<String>(){{
    add("a");
    add("b");
    add("c");
}};
```
