###  set precision for decimal and floats


[Java: How to set Precision for double value? - Stack Overflow](https://stackoverflow.com/questions/14845937/java-how-to-set-precision-for-double-value "Java: How to set Precision for double value? - Stack Overflow")


 

```java
Double toBeTruncated = new Double("3.5789055");

Double truncatedDouble = BigDecimal.valueOf(toBeTruncated)
    .setScale(3, RoundingMode.HALF_UP)
    .doubleValue();
```
