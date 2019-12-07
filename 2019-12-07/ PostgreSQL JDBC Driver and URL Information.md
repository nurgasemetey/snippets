###  PostgreSQL JDBC Driver and URL Information


[PostgreSQL JDBC Driver and URL Information](https://razorsql.com/docs/help_postgresql.html "PostgreSQL JDBC Driver and URL Information")


 

```shell

PostgreSQL Connection Help

Listed below are connection examples for PostgreSQL:

PostgreSQL Native JDBC Driver

DRIVER CLASS: org.postgresql.Driver

DRIVER LOCATION: Simply provide the location of the jar file containing the PostgreSQL JDBC Drivers. These drivers can be obtained from PostgreSQL. See the PostgreSQL web site for more information.

JDBC URL FORMAT: jdbc:postgresql://<host>:<port>/<database_name>

The default port for PostgreSQL is 5432. Usually, if the default port is being used by the database server, the :<port> value of the JDBC url can be omitted.

Examples:

jdbc:postgresql://neptune.acme.com:5432/test

jdbc:postgresql://127.0.0.1:5432/test

```
