###  gcloud cloud sql proxy


[Connecting psql client using the Cloud SQL Proxy](https://cloud.google.com/sql/docs/postgres/connect-admin-proxy "Connecting psql client using the Cloud SQL Proxy")


 

```
cloud_sql_proxy -instances=public-transportation-tto:europe-west3:transportation-data2=tcp:5432 -credential_file=./service_accounts/public-transportation-tto-db-development.json

Service account json must have
Cloud SQL Client
Cloud SQL Editor
Cloud SQL Admin
```
