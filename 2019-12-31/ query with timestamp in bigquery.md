###  query with timestamp in bigquery


[TIMESTAMP and Standard SQL in Google BigQuery - Stack Overflow](https://stackoverflow.com/questions/46399385/timestamp-and-standard-sql-in-google-bigquery "TIMESTAMP and Standard SQL in Google BigQuery - Stack Overflow")


 

```sql
SELECT
    user_id
FROM
    dataset.table
WHERE
    timestamp > TIMESTAMP('2017-09-18 00:00:00')
```
