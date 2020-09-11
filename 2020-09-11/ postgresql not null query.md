###  postgresql not null query


[postgresql - Delete from table rows where any of the column field is null - Database Administrators Stack Exchange](https://dba.stackexchange.com/questions/143959/delete-from-table-rows-where-any-of-the-column-field-is-null "postgresql - Delete from table rows where any of the column field is null - Database Administrators Stack Exchange")


 

```
select *
from the_table
where the_table is not null;

```
