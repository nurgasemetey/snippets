###  set font name in apache poi


[java - How to set a font family to an entire Word document in Apache POI XWPF - Stack Overflow](https://stackoverflow.com/questions/28437337/how-to-set-a-font-family-to-an-entire-word-document-in-apache-poi-xwpf "java - How to set a font family to an entire Word document in Apache POI XWPF - Stack Overflow")


 

```java
        XSSFFont underlineFont = (XSSFFont) sheet.getWorkbook().createFont();
        underlineFont.setBold(true);
        underlineFont.setUnderline(FontUnderline.SINGLE);
        underlineFont.setFontName("Times New Roman");
        return underlineFont;
```
