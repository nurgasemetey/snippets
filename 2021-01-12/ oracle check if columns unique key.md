###  oracle check if columns unique key


[sql - Query to determine if columns combine to create a unique key - Stack Overflow](https://stackoverflow.com/questions/10837396/query-to-determine-if-columns-combine-to-create-a-unique-key "sql - Query to determine if columns combine to create a unique key - Stack Overflow")


 

```
select t.a, t.b, t.c, count(1) 
from my_table t    
group by t.a, t.b, t.c 
having count(1) > 1;
```
