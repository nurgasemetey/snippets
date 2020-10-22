###  oracle limit


[sql - How do I limit the number of rows returned by an Oracle query after ordering? - Stack Overflow](https://stackoverflow.com/questions/470542/how-do-i-limit-the-number-of-rows-returned-by-an-oracle-query-after-ordering "sql - How do I limit the number of rows returned by an Oracle query after ordering? - Stack Overflow")


 

```
SELECT
    title
FROM
    post
ORDER BY
    id DESC
FETCH FIRST 50 ROWS ONLY
```
