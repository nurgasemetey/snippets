###  concatenate in postgresql


[concatenation - PostgreSQL concat an int value with a numeric field - Stack Overflow](https://stackoverflow.com/questions/11345065/postgresql-concat-an-int-value-with-a-numeric-field "concatenation - PostgreSQL concat an int value with a numeric field - Stack Overflow")




```sql
SELECT CAST(line_id as text) || '' || CAST(subline_id as text) as test
from public.lines
```
