###  Cql2csv query example





 

```shell
./cql2csv -c 192.168.150.123 -u cassandra -p cassandra -k tkm_fcd_cassandra -q "select * from tkm_fcd_cassandra.segment_data where organization_id='582211846abad13209524934' and day_text='2019-04-16'" > 582211846abad13209524934-2019-04-16.csv
```
