###  Mongoexport collection with query





 

```shell
mongoexport -u user -p password -d tkm_bluesense --collection Data --query "{"discoveryTime":{"\$gt": 1564261200, "\$lt" : 1564866000}, "deviceId": {"\$in": ["4261","4262", "4255", "4286", "4250"]}}" --jsonArray --out simulator.json
```

