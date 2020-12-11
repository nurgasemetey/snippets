### mongo limit documents







```
db.getCollection('ssmData').find({junctionId:"0602"}, {junctionId:1, ts:1}).limit(50);
```
