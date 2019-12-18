### on duplicate update with new value


[sql - MySQL ON DUPLICATE KEY UPDATE for multiple rows insert in single query - Stack Overflow](https://stackoverflow.com/questions/2714587/mysql-on-duplicate-key-update-for-multiple-rows-insert-in-single-query "sql - MySQL ON DUPLICATE KEY UPDATE for multiple rows insert in single query - Stack Overflow")




```sql
INSERT INTO beautiful (name, age)
    VALUES
    ('Helen', 24),
    ('Katrina', 21),
    ('Samia', 22),
    ('Hui Ling', 25),
    ('Yumie', 29)
ON DUPLICATE KEY UPDATE
    age = VALUES(age),
     ...
```
