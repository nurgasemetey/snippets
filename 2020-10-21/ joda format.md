###  joda format


[java - How to format Joda-Time DateTime to only mm/dd/yyyy? - Stack Overflow](https://stackoverflow.com/questions/20331163/how-to-format-joda-time-datetime-to-only-mm-dd-yyyy "java - How to format Joda-Time DateTime to only mm/dd/yyyy? - Stack Overflow")


 

```
String dateTime = "11/15/2013 08:00:00";
// Format for input
DateTimeFormatter dtf = DateTimeFormat.forPattern("MM/dd/yyyy HH:mm:ss");
// Parsing the date
DateTime jodatime = dtf.parseDateTime(dateTime);
// Format for output
DateTimeFormatter dtfOut = DateTimeFormat.forPattern("MM/dd/yyyy");
// Printing the date
System.out.println(dtfOut.print(jodatime));

```
