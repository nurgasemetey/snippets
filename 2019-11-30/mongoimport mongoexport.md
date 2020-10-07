### mongoimport mongoexport


[Insert json file into mongodb - Stack Overflow](https://stackoverflow.com/questions/19441228/insert-json-file-into-mongodb "Insert json file into mongodb - Stack Overflow")




```shell
mongoimport --jsonArray --db test --collection docs --file example2.json


mongoexport -u parabol -p parabol --db kgm --collection Fisibility --jsonArray --out Fisibility.json --authenticationDatabase kgm

mongoimport -u parabol -p parabol --db kgm --collection Fisibility --jsonArray --file new-feasibility.json --authenticationDatabase kgm

```
