###  list to array in java


[arrays - Converting 'ArrayList&lt;String&gt; to 'String\[\]' in Java - Stack Overflow](https://stackoverflow.com/questions/4042434/converting-arrayliststring-to-string-in-java "arrays - Converting 'ArrayList&lt;String&gt; to 'String[]' in Java - Stack Overflow")


 

```java
String[] strings = list.stream().toArray(String[]::new);

```
