###  cassandra csv





 

```
./cql2csv -c 192.168.150.123 -u username -p password -k tkm_fcd_cassandra -q "select * from tkm_fcd_cassandra.segment_data where organization_id='57ecdd14766299a02213c463' and day_text='2019-01-17'"


cqlsh -u username -p password -e "select * from tkm_fcd_cassandra.segment_data where organization_id='57ecdd14766299a02213c463' and day_text='2019-01-17'"
```
