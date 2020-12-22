###  log4j xml date


[java - changing date format in log4j.xml - Stack Overflow](https://stackoverflow.com/questions/21979606/changing-date-format-in-log4j-xml/21979657 "java - changing date format in log4j.xml - Stack Overflow")


 

```
<!-- Appenders -->
<appender name="console" class="org.apache.log4j.ConsoleAppender">
    <param name="Target" value="System.out" />
    <layout class="XXX">
        <param name="ConversionPattern" value="%d{yyyy-MM-dd HH:mm:ss} %-5p [%c{1}] (%t) [%X] %m%n" />
    </layout>
</appender>
```
