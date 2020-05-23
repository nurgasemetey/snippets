###  dump, restore postgresql
[How to generate a Postgresql Dump from a Docker container? - Stack Overflow](https://stackoverflow.com/questions/30171063/how-to-generate-a-postgresql-dump-from-a-docker-container "How to generate a Postgresql Dump from a Docker container? - Stack Overflow")

[postgresql - pg_restore in postgres docker container - Stack Overflow](https://stackoverflow.com/questions/39267377/pg-restore-in-postgres-docker-container "postgresql - pg_restore in postgres docker container - Stack Overflow")




 

```bash

docker exec some-postgres pg_dump -U postgres -F t investment_app > investment_app-2020-05-12.sql
docker exec some-postgres pg_dump -U postgres -F t internal_control_app > internal_control_app-2020-05-12.sql

docker exec -i some-postgres pg_restore -U postgres -v -d investment_app < investment_app-2020-05-12.sql
docker exec -i some-postgres pg_restore -U postgres -v -d internal_control_app < internal_control_app-2020-05-12.sql

```
