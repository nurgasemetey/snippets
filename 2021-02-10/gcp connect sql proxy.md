### gcp connect sql proxy





 

```
./cloud_sql_proxy -instances=instances:region:gis=tcp:5432 -credential_file= &
psql "host=127.0.0.1 sslmode=disable dbname=db user=user
```
