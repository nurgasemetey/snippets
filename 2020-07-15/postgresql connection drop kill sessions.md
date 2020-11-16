### postgresql connection drop kill sessions


[How to drop a PostgreSQL database if there are active connections to it? - Stack Overflow](https://stackoverflow.com/questions/5408156/how-to-drop-a-postgresql-database-if-there-are-active-connections-to-it "How to drop a PostgreSQL database if there are active connections to it? - Stack Overflow")

[postgresql - Drop a database being accessed by another users? - Stack Overflow](https://stackoverflow.com/questions/664091/drop-a-database-being-accessed-by-another-users "postgresql - Drop a database being accessed by another users? - Stack Overflow")


```sql
SELECT pg_terminate_backend(pg_stat_activity.pid)
FROM pg_stat_activity
WHERE pg_stat_activity.datname = 'TARGET_DB' -- ← change this to your DB
  AND pid <> pg_backend_pid();



also

Simplest fix for this is restart the postgresql. After that You can get rid of database!


```
