###  Convert Long into Integer


[java - Convert Long into Integer - Stack Overflow](https://stackoverflow.com/questions/5804043/convert-long-into-integer "java - Convert Long into Integer - Stack Overflow")


 

```java
Integer intVal = longVal == null ? null : Math.toIntExact(longVal);

```
