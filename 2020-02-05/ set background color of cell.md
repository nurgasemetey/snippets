###  set background color of cell


[Java Apache Poi, how to set background color and borders at same time - Stack Overflow](https://stackoverflow.com/questions/38874115/java-apache-poi-how-to-set-background-color-and-borders-at-same-time "Java Apache Poi, how to set background color and borders at same time - Stack Overflow")


 

```java
CellStyle cs = wb.createCellStyle();
cs.setFillForegroundColor(IndexedColors.GREY_25_PERCENT.getIndex());
cs.setFillPattern(FillPatternType.SOLID_FOREGROUND);

```
