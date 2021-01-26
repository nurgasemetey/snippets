### postgresql duplicate rows


[sql - How to find duplicate records in PostgreSQL - Stack Overflow](https://stackoverflow.com/questions/28156795/how-to-find-duplicate-records-in-postgresql "sql - How to find duplicate records in PostgreSQL - Stack Overflow")


 

```
select Column1, Column2, count(*)
from yourTable
group by Column1, Column2
HAVING count(*) > 1
```
