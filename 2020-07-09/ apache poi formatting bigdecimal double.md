###  apache poi formatting bigdecimal double


[java - Apache-poi decimal formatting is being applied only after selection - Stack Overflow](https://stackoverflow.com/questions/56292456/apache-poi-decimal-formatting-is-being-applied-only-after-selection "java - Apache-poi decimal formatting is being applied only after selection - Stack Overflow")


 

```
Simply do not set cell value as string if you need a numeric cell value. If you set cell value as String, then the cell type also will be string. This is independent of setting CellType before setting cell value. While setting a String cell value the type changes to string always.


```
