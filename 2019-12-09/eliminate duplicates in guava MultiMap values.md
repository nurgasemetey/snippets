### eliminate duplicates in guava MultiMap values


[java - How to eliminate duplicates in Guava MultiMap values? - Stack Overflow](https://stackoverflow.com/questions/18983463/how-to-eliminate-duplicates-in-guava-multimap-values "java - How to eliminate duplicates in Guava MultiMap values? - Stack Overflow")


 

```
SetMultimap<String, String> myMultimap = HashMultimap.create();
myMultimap.put("12345", "qwer");
myMultimap.put("12345", "abcd");
myMultimap.put("12345", "qwer");
System.out.println(myMultimap); // {12345=[abcd, qwer]}
```
