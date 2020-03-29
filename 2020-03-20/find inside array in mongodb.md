### find inside array in mongodb


[$elemMatch (query) — MongoDB Manual](https://docs.mongodb.com/manual/reference/operator/query/elemMatch "$elemMatch (query) — MongoDB Manual")


 

```js
db.getCollection('errorData').find({ errors : { $elemMatch : { _id : 104}}}).count()
```
