### cassandra export csv with query







```
Using tool - https://github.com/tenmax/cqlkit


./cql2csv -c ip -u user -p password -k keyspace -q "select * from keyspace.table where organization_id='orgid' and day_text='2019-04-16'" > orgid-2019-04-16.csv

```
