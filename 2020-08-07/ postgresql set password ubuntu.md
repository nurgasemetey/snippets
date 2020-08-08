###  postgresql set password ubuntu


[Connecting to PostgreSQL on Linux for the first time — Boundless Server 1.1.1 User Manual](https://docs.boundlessgeo.com/suite/1.1.1/dataadmin/pgGettingStarted/firstconnect.html "Connecting to PostgreSQL on Linux for the first time — Boundless Server 1.1.1 User Manual")


 

```
To set the default password:

Run the psql command from the postgres user account:

sudo -u postgres psql postgres
Set the password:

\password postgres
Enter a password.

Close psql.

\q
```
