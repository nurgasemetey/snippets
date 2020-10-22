###  mongodb except





 

```
db.getCollection('phaseData').find({junctionId: { $nin: ["112233", "1"] },detectorDatas:{$ne: []}}).sort({$natural:-1})
```
