###  Create user mysql and grant privileges





 

```sql
CREATE USER 'root'@'%' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON * . * TO 'root'@'%';
```
