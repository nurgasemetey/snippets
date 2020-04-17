###  How to Sum BigDecimal using Stream


[Java 8 – How to Sum BigDecimal using Stream? – Mkyong.com](https://mkyong.com/java8/java-8-how-to-sum-bigdecimal-using-stream/ "Java 8 – How to Sum BigDecimal using Stream? – Mkyong.com")


 

```java
        List<Invoice> invoices = Arrays.asList(
                new Invoice("I1001", BigDecimal.valueOf(9.99), BigDecimal.valueOf(1)),
                new Invoice("I1002", BigDecimal.valueOf(19.99), BigDecimal.valueOf(1.5)),
                new Invoice("I1003", BigDecimal.valueOf(4.888), BigDecimal.valueOf(2)),
                new Invoice("I1004", BigDecimal.valueOf(4.99), BigDecimal.valueOf(5)),
                new Invoice("I1005", BigDecimal.valueOf(.5), BigDecimal.valueOf(2.3))
        );

        BigDecimal sum = invoices.stream()
                .map(x -> x.getQty().multiply(x.getPrice()))    // map
                .reduce(BigDecimal.ZERO, BigDecimal::add);      // reduce
```
