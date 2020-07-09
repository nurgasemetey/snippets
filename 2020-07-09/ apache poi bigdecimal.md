###  apache poi bigdecimal


[How to store BigDecimal in Excel file Using Java - Stack Overflow](https://stackoverflow.com/questions/41374772/how-to-store-bigdecimal-in-excel-file-using-java "How to store BigDecimal in Excel file Using Java - Stack Overflow")


 

```java
cell_1.setCellValue(resultSet.getBigDecimal("longitude").toPlainString());


 if(value instanceof BigDecimal) {
            cell.setCellValue(((BigDecimal) value).toPlainString());
        }
```
