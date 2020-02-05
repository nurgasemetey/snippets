###  trip space in postgresql


[postgresql - How do I remove all spaces from a field in a Postgres database in an update query? - Stack Overflow](https://stackoverflow.com/questions/20376579/how-do-i-remove-all-spaces-from-a-field-in-a-postgres-database-in-an-update-quer "postgresql - How do I remove all spaces from a field in a Postgres database in an update query? - Stack Overflow")


 

```sql
update users
  set fullname = replace(fullname, ' ', '');
commit;
```
