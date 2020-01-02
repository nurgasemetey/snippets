###  group time intervals in bigquery


[mysql - How to group by time intervals with Google BigQuery - Stack Overflow](https://stackoverflow.com/questions/55191664/how-to-group-by-time-intervals-with-google-bigquery "mysql - How to group by time intervals with Google BigQuery - Stack Overflow")


 

```sql
#standardSQL
SELECT 
  TIMESTAMP_SECONDS(15*60 * DIV(UNIX_SECONDS(utc_timestamp), 15*60)) timekey,
  AVG(metric) metric
FROM `project.dataset.table`
GROUP BY timekey
```
