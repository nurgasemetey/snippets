###  postgresql on duplicate on conflict update


[sql - Insert, on duplicate update in PostgreSQL? - Stack Overflow](https://stackoverflow.com/questions/1109061/insert-on-duplicate-update-in-postgresql "sql - Insert, on duplicate update in PostgreSQL? - Stack Overflow")



[PostgreSQL Upsert Using INSERT ON CONFLICT statement](https://www.postgresqltutorial.com/postgresql-upsert/ "PostgreSQL Upsert Using INSERT ON CONFLICT statement")


 

```
INSERT INTO the_table (id, column_1, column_2) 
VALUES (1, 'A', 'X'), (2, 'B', 'Y'), (3, 'C', 'Z')
ON CONFLICT (id) DO UPDATE 
  SET column_1 = excluded.column_1, 
      column_2 = excluded.column_2;


INSERT INTO user_info(user_id, access_token, refresh_token) VALUES($1, $2, $3) ON CONFLICT (user_id) DO UPDATE SET access_token = excluded.access_token, refresh_token = excluded.refresh_token
```
