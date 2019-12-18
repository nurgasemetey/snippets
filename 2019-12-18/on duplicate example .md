### on duplicate example 


[MySQL INSERT ON DUPLICATE KEY UPDATE](http://www.mysqltutorial.org/mysql-insert-or-update-on-duplicate-key-update/ "MySQL INSERT ON DUPLICATE KEY UPDATE")


 

```sql
INSERT INTO table (column_list)
VALUES (value_list)
ON DUPLICATE KEY UPDATE
   c1 = v1, 
   c2 = v2,
   ...;
```
