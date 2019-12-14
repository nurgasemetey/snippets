### Calendar with UTC time


[java - How can I set a Calendar with UTC time? - Stack Overflow](https://stackoverflow.com/questions/6059207/how-can-i-set-a-calendar-with-utc-time "java - How can I set a Calendar with UTC time? - Stack Overflow")




```java
Calendar calendar = Calendar.getInstance(TimeZone.getTimeZone("UTC"));

```
