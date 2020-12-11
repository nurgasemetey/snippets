### postgresql postgis create index on geometry field





 

```
CREATE INDEX my_table_geom_idx
  ON my_table
  USING gist(geom);
```
