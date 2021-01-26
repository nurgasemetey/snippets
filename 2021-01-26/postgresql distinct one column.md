### postgresql distinct one column


[postgresql - Postgres: Distinct but only for one column - Stack Overflow](https://stackoverflow.com/questions/16913969/postgres-distinct-but-only-for-one-column "postgresql - Postgres: Distinct but only for one column - Stack Overflow")


 

```
select distinct on (name)
    name, col1, col2
from names

---
 select distinct on(geometry_info.kkno) kkno,
jsonb_array_elements(geometry_info.geometry -> 'features') AS feat
 geometry_info.project_id
from geometry_info
```
