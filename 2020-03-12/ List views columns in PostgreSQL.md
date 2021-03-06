###  List views columns in PostgreSQL


[List views columns in PostgreSQL - PostgreSQL Data Dictionary Queries](https://dataedo.com/kb/query/postgresql/list-views-columns "List views columns in PostgreSQL - PostgreSQL Data Dictionary Queries")


 

```SQL
select t.table_schema as schema_name,
       t.table_name as view_name,
       c.column_name,
       c.data_type,
       case when c.character_maximum_length is not null
            then c.character_maximum_length
            else c.numeric_precision end as max_length,
       is_nullable
       from information_schema.tables t
    left join information_schema.columns c 
              on t.table_schema = c.table_schema 
              and t.table_name = c.table_name
where table_type = 'VIEW' 
      and t.table_schema not in ('information_schema', 'pg_catalog')
order by schema_name,
         view_name;
```
