###  possibly consider using a shorter maxlifetime


[spring boot - HikariPool-1 - Failed to validate connection org.postgresql.jdbc.PgConnection@2a84e649 (This connection has been closed.) - Stack Overflow](https://stackoverflow.com/questions/52536053/hikaripool-1-failed-to-validate-connection-org-postgresql-jdbc-pgconnection2a "spring boot - HikariPool-1 - Failed to validate connection org.postgresql.jdbc.PgConnection@2a84e649 (This connection has been closed.) - Stack Overflow")


 

```yml
spring.datasource.hikari.maxLifetime=1800000
```
