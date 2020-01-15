###  cell border in apache poi

[java - Add borders to cells in POI generated Excel File - Stack Overflow](https://stackoverflow.com/questions/5720049/add-borders-to-cells-in-poi-generated-excel-file "java - Add borders to cells in POI generated Excel File - Stack Overflow")




```java
        XSSFCellStyle dataCellStyle = workbook.createCellStyle();
        dataCellStyle.setBorderTop(BorderStyle.THIN);
        dataCellStyle.setBorderBottom(BorderStyle.THIN);
        dataCellStyle.setBorderLeft(BorderStyle.THIN);
        dataCellStyle.setBorderRight(BorderStyle.THIN);

		XSSFFont font = workbook.createFont();
        font.setBold(true);
        columnCellStyle.setFont(font);

		cell.setCellStyle(dataCellStyle);
```
