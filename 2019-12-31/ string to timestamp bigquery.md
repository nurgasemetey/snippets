###  string to timestamp bigquery


[mysql - Converting string column to timestamp in BigQuery? - Stack Overflow](https://stackoverflow.com/questions/54897389/converting-string-column-to-timestamp-in-bigquery "mysql - Converting string column to timestamp in BigQuery? - Stack Overflow")


 

```sql
PARSE_TIMESTAMP("%Y%m%d%k%M", utc_timestamp)

```
