###  add borders to cell range in apache poi


[JAVA Apache POI Excel: add borders to cell range - Stack Overflow](https://stackoverflow.com/questions/28564967/java-apache-poi-excel-add-borders-to-cell-range "JAVA Apache POI Excel: add borders to cell range - Stack Overflow")


 

```java
CellRangeAddress region = new CellRangeAddress(6, 8, 1, 10);
RegionUtil.setBorderBottom(BorderStyle.THIN, region, sheet);
RegionUtil.setBorderTop(BorderStyle.THIN, region, sheet);
RegionUtil.setBorderLeft(BorderStyle.THIN, region, sheet);
RegionUtil.setBorderRight(BorderStyle.THIN, region, sheet);
```
