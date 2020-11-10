###  jodate difference duration


[java - How to find difference between two Joda-Time DateTimes in minutes - Stack Overflow](https://stackoverflow.com/questions/12851934/how-to-find-difference-between-two-joda-time-datetimes-in-minutes "java - How to find difference between two Joda-Time DateTimes in minutes - Stack Overflow")


 

```
DateTime today = new DateTime();
DateTime yesterday = today.minusDays(1);

Duration duration = new Duration(yesterday, today);
System.out.println(duration.getStandardDays());
System.out.println(duration.getStandardHours());
System.out.println(duration.getStandardMinutes());
```
