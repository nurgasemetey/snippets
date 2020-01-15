###  merge cells in apache poi


[java - Merging cells in Excel using Apache POI - Stack Overflow](https://stackoverflow.com/questions/18716032/merging-cells-in-excel-using-apache-poi "java - Merging cells in Excel using Apache POI - Stack Overflow")


 

```java
sheet.addMergedRegion(new CellRangeAddress(startRowIndx, endRowIndx, startColIndx,endColIndx));

```
