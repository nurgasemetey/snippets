###  create table sql postgresql


[PostgreSQL CREATE TABLE](http://www.postgresqltutorial.com/postgresql-create-table/)

[Multiple primary keys in PostgreSQL - Database Administrators Stack Exchange](https://dba.stackexchange.com/questions/65289/multiple-primary-keys-in-postgresql "Multiple primary keys in PostgreSQL - Database Administrators Stack Exchange")
 

```sql
CREATE TABLE role(
   role_id serial PRIMARY KEY,
   role_name VARCHAR (255) UNIQUE NOT NULL
);

CREATE TABLE mytable (
    field1 INTEGER,
    field2 INTEGER,
    PRIMARY KEY (field1, field2)
);
```
