###  mongodb remove field


[How to remove a field completely from a MongoDB document? - Stack Overflow](https://stackoverflow.com/questions/6851933/how-to-remove-a-field-completely-from-a-mongodb-document "How to remove a field completely from a MongoDB document? - Stack Overflow")


 

```
db.example.updateMany({},{"$unset":{"tags.words":1}})
db.getCollection('Request').updateMany({},{"$unset":{"totals":1}})
db.getCollection('Section').updateMany({},{"$unset":{"totals":1}})
```
