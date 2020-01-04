###  Docker mongoexport example


[](https://stackoverflow.com/questions/41892753/how-to-export-mongo-database-using-docker "node.js - How to export Mongo-database using Docker? - Stack Overflow")


 

```shell
docker exec -i amazing_diffie mongoexport -u {} -p {} --db metistraffic --collection ssmData --query '{"junctionId":"118","ts" : {$lte: ISODate("2017-06-18T03:00:00.000Z")}}' --authenticationDatabase metistraffic 2>/tmp/mongoexport.err > ssmdata.json
```
