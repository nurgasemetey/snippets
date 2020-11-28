###  set currency in apache poi


[Set Data Format in Excel Using POI 3.0](https://www.roseindia.net/java/poi/setDataFormat.shtml "Set Data Format in Excel Using POI 3.0")



[java - Formatting Excel cell as Dollar with Apache POI where the machine currency is not dollar - Stack Overflow](https://stackoverflow.com/questions/24763383/formatting-excel-cell-as-dollar-with-apache-poi-where-the-machine-currency-is-no "java - Formatting Excel cell as Dollar with Apache POI where the machine currency is not dollar - Stack Overflow")


[java - Apache poi - Thousand separator - Stack Overflow](https://stackoverflow.com/questions/14876548/apache-poi-thousand-separator "java - Apache poi - Thousand separator - Stack Overflow")

[java - Cell formatting to remove decimal point in excel cell when data Writing Using Apache POI - Stack Overflow](https://stackoverflow.com/questions/43575608/cell-formatting-to-remove-decimal-point-in-excel-cell-when-data-writing-using-ap "java - Cell formatting to remove decimal point in excel cell when data Writing Using Apache POI - Stack Overflow")

 

```java
        DataFormat format = sheet.getWorkbook().createDataFormat();
        cellStyle.setDataFormat(format.getFormat("₺#,##0.00"));
```
