###  postgresql timestamp query


[postgresql - Postgres where clause compare timestamp - Stack Overflow](https://stackoverflow.com/questions/31433747/postgres-where-clause-compare-timestamp "postgresql - Postgres where clause compare timestamp - Stack Overflow")


 

```sql
select *
from the_table
where the_timestamp_column >= timestamp '2015-07-15 00:00:00'
  and the_timestamp_column < timestamp '2015-07-16 00:00:00';


SELECT site_reference_id, ts, mean_vehicle_flow 
FROM public.travelspeed where ts=CAST('2020-05-14 05:12:00' as timestamp without time zone);

```
