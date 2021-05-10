### postgresql isnull


[sql server - What is the PostgreSQL equivalent for ISNULL() - Stack Overflow](https://stackoverflow.com/questions/2214525/what-is-the-postgresql-equivalent-for-isnull "sql server - What is the PostgreSQL equivalent for ISNULL() - Stack Overflow")


 

```
SELECT coalesce(field, 'Empty') AS field_alias
select teacher_name, coalesce(student_size.cnt, 0) as cnt
```
