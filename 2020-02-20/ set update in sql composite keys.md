###  set update in sql composite keys


[WHERE col1,col2 IN (...) \[SQL subquery using composite primary key\] - Stack Overflow](https://stackoverflow.com/questions/4622453/where-col1-col2-in-sql-subquery-using-composite-primary-key "WHERE col1,col2 IN (...) [SQL subquery using composite primary key] - Stack Overflow")


 

```sql
SELECT * 
  FROM foo 
  WHERE (a, b) IN (
                   SELECT a, b 
                      FROM bar
                  );

UPDATE public.investment
	SET is_child=true 
	where (project_id,working_year) in (
	SELECT project_id, working_year
FROM investment AS f1
WHERE NOT EXISTS (
  SELECT 1
  FROM investment AS f2
  WHERE f1.path <> f2.path
    AND f1.path @> f2.path
));

```
