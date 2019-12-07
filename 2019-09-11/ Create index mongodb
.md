###  Create index mongodb



[db.collection.createIndex() — MongoDB Manual](https://docs.mongodb.com/manual/reference/method/db.collection.createIndex)


 

```shell
db.getCollection('statusData').createIndex( { junctionId: 1, ts : -1}, {background: true} );
```
