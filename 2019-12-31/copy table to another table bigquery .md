### copy table to another table bigquery 





 

```sql
INSERT
  `kgm-traffic-221812.smart_mobility.travel_time`(start_node,
    finish_node,
    speed,
    travel_time,
    ts)
SELECT
  start_node,
  finish_node,
  speed,
  travel_time,
  PARSE_TIMESTAMP("%Y-%m-%d %H:%M:%S%Ez", ts)
FROM
  `kgm-traffic-221812.smart_mobility.travel_time_tmp`
LIMIT
  10
 
##bigquery

INSERT
  `public-transportation-tto.fcd.segment_data`(some_id,
    segment_id,
    travel_time,
    coverage,
    ts )
SELECT
  some_id,
  segment_id,
  travel_time,
  cast(SPLIT(coverage_and_ts, ',')[
OFFSET
  (0)] as int64),
  TIMESTAMP(SPLIT(coverage_and_ts, ',')[
OFFSET
  (1)])
FROM (
  SELECT
    some_id,
    segment_id,
    travel_time,
    coverage_and_ts
  FROM
    `public-transportation-tto.fcd.segment_data_tmp`
  LIMIT
    10 )


```

