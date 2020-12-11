### finding line number of expression







```
lineNumber=$(awk "/\[mysqld\]/{ print NR; exit }" /etc/mysql/my.cnf)
```
