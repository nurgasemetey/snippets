###  dump, restore postgresql





 

```bash

docker exec some-postgres pg_dump -U postgres -F t investment_app > investment_app-2020-05-12.sql
docker exec some-postgres pg_dump -U postgres -F t internal_control_app > internal_control_app-2020-05-12.sql

docker exec -i some-postgres pg_restore -U postgres -v -d investment_app < investment_app-2020-05-12.sql
docker exec -i some-postgres pg_restore -U postgres -v -d internal_control_app < internal_control_app-2020-05-12.sql

```
