###  postgresql session list


[List sessions / active connections in PostgreSQL database - PostgreSQL Data Dictionary Queries](https://dataedo.com/kb/query/postgresql/list-database-sessions "List sessions / active connections in PostgreSQL database - PostgreSQL Data Dictionary Queries")


 

```sql
select pid as process_id, 
       usename as username, 
       datname as database_name, 
       client_addr as client_address, 
       application_name,
       backend_start,
       state,
       state_change
from pg_stat_activity;
```
