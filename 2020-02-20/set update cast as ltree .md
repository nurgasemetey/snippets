### set update cast as ltree 


[postgresql - SQL: How do I update a value inside of an ltree? - Stack Overflow](https://stackoverflow.com/questions/28259805/sql-how-do-i-update-a-value-inside-of-an-ltree "postgresql - SQL: How do I update a value inside of an ltree? - Stack Overflow")




```sql
UPDATE public.investment
	SET path=public.investment.investment_code::ltree;
```
