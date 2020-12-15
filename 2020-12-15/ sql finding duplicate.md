###  sql finding duplicate


[Finding duplicate values in a SQL table - Stack Overflow](https://stackoverflow.com/questions/2594829/finding-duplicate-values-in-a-sql-table "Finding duplicate values in a SQL table - Stack Overflow")


 

```
SELECT name, email
FROM users
GROUP BY name, email
HAVING ( COUNT(*) > 1 )

```
