###  Create table


[PostgreSQL CREATE TABLE](http://www.postgresqltutorial.com/postgresql-create-table/)


 

```sql
CREATE TABLE role(
   role_id serial PRIMARY KEY,
   role_name VARCHAR (255) UNIQUE NOT NULL
);
```
