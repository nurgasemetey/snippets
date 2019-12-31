### copy table to another table bigquery 





 

```sql
 insert `kgm-traffic-221812.smart_mobility.travel_time`(start_node, finish_node, speed, travel_time, ts) SELECT start_node, finish_node, speed, travel_time, PARSE_TIMESTAMP("%Y-%m-%d %H:%M:%S%Ez", ts) FROM `kgm-traffic-221812.smart_mobility.travel_time_tmp` LIMIT 10
```
