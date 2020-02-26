### ltree levels in postgresql


[sql - How to create hierarchal json object using ltree query results? (postgresql) - Stack Overflow](https://stackoverflow.com/questions/47092583/how-to-create-hierarchal-json-object-using-ltree-query-results-postgresql "sql - How to create hierarchal json object using ltree query results? (postgresql) - Stack Overflow")




```sql
select id,path, nlevel(subpath(path, 1)) as node_level from test
```
