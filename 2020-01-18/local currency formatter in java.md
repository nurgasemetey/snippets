### local currency formatter in java, fraction limit


[Java NumberFormat - formatting numbers and currencies in Java](http://zetcode.com/java/numberformat/ "Java NumberFormat - formatting numbers and currencies in Java")




```java
static NumberFormat costFormat = NumberFormat.getCurrencyInstance(new Locale("tr","TR"));
costFormat.setMinimumFractionDigits(2);
costFormat.setMaximumFractionDigits(4);
```
