### How to export sorted data using mongoexport


[mongodb - How to export sorted data using mongoexport? - Stack Overflow](https://stackoverflow.com/questions/9005983/how-to-export-sorted-data-using-mongoexport "mongodb - How to export sorted data using mongoexport? - Stack Overflow")




```shell
mongoexport  -q '{ $query: {count: {$gt:0}}, $orderby: {count: -1} }' -d database -c collection > data_dump.json
mongoexport -h 192.168.1.18 -u parabol -p parabol --db tkm_bluesense --collection TravelTime --query '{vectorId:"42014234", ts:{$gte: 1551240000000, $lte:1551259740000}}' --fields "sourceSensor,destinationSensor,distance" --sort "{ts: 1}" --csv --out Vector.csv --authenticationDatabase tkm_bluesense
```

