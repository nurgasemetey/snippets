###  Inner join


[SQL Joins](https://www.w3schools.com/sql/sql_join.asp)


 

```sql
SELECT hat_durak.*, duraklar.*
FROM hat_durak
INNER JOIN duraklar ON hat_durak."DURAK_ID"=duraklar."DURAK_NO" and hat_durak."HAT_ID"=443;

```
