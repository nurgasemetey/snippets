###  set background color of cell


[Java Apache Poi, how to set background color and borders at same time - Stack Overflow](https://stackoverflow.com/questions/38874115/java-apache-poi-how-to-set-background-color-and-borders-at-same-time "Java Apache Poi, how to set background color and borders at same time - Stack Overflow")

[excel - Java Apache POI - XSSFCell setFillBackgroundColor Has No Effect - Stack Overflow](https://stackoverflow.com/questions/45536432/java-apache-poi-xssfcell-setfillbackgroundcolor-has-no-effect "excel - Java Apache POI - XSSFCell setFillBackgroundColor Has No Effect - Stack Overflow")


```java
CellStyle cs = wb.createCellStyle();
style.setFillForegroundColor(color);
style.setFillPattern(FillPatternType.SOLID_FOREGROUND);
cell.setCellStyle(style);
```
