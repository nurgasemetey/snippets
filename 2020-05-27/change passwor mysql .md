### change passwor mysql 


[upgrade - Updating MySQL passwords for 5.6? - Stack Overflow](https://stackoverflow.com/questions/22171542/updating-mysql-passwords-for-5-6 "upgrade - Updating MySQL passwords for 5.6? - Stack Overflow")


 

```
shell> mysql -u root
mysql> SET PASSWORD FOR 'root'@'localhost' = PASSWORD('newpwd');
mysql> SET PASSWORD FOR 'root'@'127.0.0.1' = PASSWORD('newpwd');
mysql> SET PASSWORD FOR 'root'@'::1' = PASSWORD('newpwd');
mysql> SET PASSWORD FOR 'root'@'host_name' = PASSWORD('newpwd');
```
