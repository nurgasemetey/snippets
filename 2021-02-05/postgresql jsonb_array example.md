### postgresql jsonb_array example





 

```
 select distinct on(geometry_info.kkno) kkno,
(jsonb_array_elements(geometry_info.geometry -> 'features') AS feat) ->> 'geometry' AS geometry,
 geometry_info.project_id
from geometry_info
```
