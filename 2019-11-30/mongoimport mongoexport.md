### mongoimport mongoexport


[Insert json file into mongodb - Stack Overflow](https://stackoverflow.com/questions/19441228/insert-json-file-into-mongodb "Insert json file into mongodb - Stack Overflow")

[mongodb - How to export sorted data using mongoexport? - Stack Overflow](https://stackoverflow.com/questions/9005983/how-to-export-sorted-data-using-mongoexport "mongodb - How to export sorted data using mongoexport? - Stack Overflow")



```shell
mongoimport --jsonArray --db test --collection docs --file example2.json


mongoexport -u user -p password --db kgm --collection Fisibility --jsonArray --out Fisibility.json --authenticationDatabase kgm

mongoimport -u user -p password --db kgm --collection Fisibility --jsonArray --file new-feasibility.json --authenticationDatabase kgm


mongoexport  -q '{ $query: {count: {$gt:0}}, $orderby: {count: -1} }' -d database -c collection > data_dump.json
mongoexport -h 192.168.1.18 -u user -p password --db tkm_bluesense --collection TravelTime --query '{vectorId:"42014234", ts:{$gte: 1551240000000, $lte:1551259740000}}' --fields "sourceSensor,destinationSensor,distance" --sort "{ts: 1}" --csv --out Vector.csv --authenticationDatabase tkm_bluesense


```
