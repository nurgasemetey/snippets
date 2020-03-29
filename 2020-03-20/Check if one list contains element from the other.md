### Check if one list contains element from the other


[java - Check if one list contains element from the other - Stack Overflow](https://stackoverflow.com/questions/11796371/check-if-one-list-contains-element-from-the-other "java - Check if one list contains element from the other - Stack Overflow")


 

```java
boolean var = lis1.stream().anyMatch(element -> list2.contains(element));

```
