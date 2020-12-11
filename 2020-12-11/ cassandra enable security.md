###  cassandra enable security


[NoSQL: &quot;org.apache.cassandra.auth.CassandraRoleManager doesn't support PASSWORD&quot;](https://www.dbrnd.com/2016/05/nosql-org-apache-cassandra-auth-cassandrarolemanager-doesnt-support-password/ "NoSQL: &quot;org.apache.cassandra.auth.CassandraRoleManager doesn't support PASSWORD&quot;")


 

```
Open /etc/cassandra/cassandra.yml

authenticator: AllowAllAuthenticator
Change with this new value:

authenticator: PasswordAuthenticator
```
