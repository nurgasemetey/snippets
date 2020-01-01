###  Bigquery read example from query


[How to use BigQuery Standard SQL in Dataflow? - Stack Overflow](https://stackoverflow.com/questions/38483778/how-to-use-bigquery-standard-sql-in-dataflow/41184675#41184675 "How to use BigQuery Standard SQL in Dataflow? - Stack Overflow")


 

```java
PCollection<TableRow> weatherData = p.apply(
BigQueryIO.Read
.named("ReadYearAndTemp")
.fromQuery("SELECT year, mean_temp FROM `samples.weather_stations`")
.usingStandardSql();
```
