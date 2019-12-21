###  output to file in mysql


[How to save MySQL query output to excel or .txt file? - Stack Overflow](https://stackoverflow.com/questions/21253704/how-to-save-mysql-query-output-to-excel-or-txt-file)


 

```sql
SELECT order_id,product_name,qty FROM orders
INTO OUTFILE '/tmp/orders.csv'
FIELDS TERMINATED BY ','
ENCLOSED BY '"'
LINES TERMINATED BY '\n'
```
