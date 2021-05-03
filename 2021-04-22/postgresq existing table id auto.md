### postgresq existing table id auto


[How to add an auto-incrementing primary key to an existing table, in PostgreSQL? - Stack Overflow](https://stackoverflow.com/questions/2944499/how-to-add-an-auto-incrementing-primary-key-to-an-existing-table-in-postgresql/30021018 "How to add an auto-incrementing primary key to an existing table, in PostgreSQL? - Stack Overflow")


 

```
ALTER TABLE test1 ADD COLUMN id SERIAL PRIMARY KEY;

```
