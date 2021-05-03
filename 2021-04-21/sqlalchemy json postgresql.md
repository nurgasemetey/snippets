### sqlalchemy json postgresql


[Using JSON Extensions in PostgreSQL from Python - Compose Articles](https://www.compose.com/articles/using-json-extensions-in-postgresql-from-python-2/ "Using JSON Extensions in PostgreSQL from Python - Compose Articles")


 

```
from sqlalchemy import Column, Integer, Text  
from sqlalchemy.dialects.postgresql import JSON, JSONB

sqlalchemy.Table("jsontable", meta,  
                Column('id', Integer),
                Column('name', Text),
                Column('email', Text),
                Column('doc', JSON))
meta.create_all()  
```
