### mongo sort insertion order natural







```
db.getCollection('ssmData').find({junctionId:"0602"}, {junctionId:1, ts:1}).sort({$natural: -1})

```
