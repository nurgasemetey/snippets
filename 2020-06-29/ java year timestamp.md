###  java year timestamp


[java - how to retrieve day month and year from Timestamp(long format) - Stack Overflow](https://stackoverflow.com/questions/6262570/how-to-retrieve-day-month-and-year-from-timestamplong-format "java - how to retrieve day month and year from Timestamp(long format) - Stack Overflow")


 

```java
if(feasibilityInfo.get("openningYear") != null) {
                Long openningYear = (Long) feasibilityInfo.get("openningYear");
                LocalDateTime ldt = Instant.ofEpochMilli(openningYear).atZone(ZoneId.systemDefault()).toLocalDateTime();
                workingYear =ldt.getYear();
            }
```
