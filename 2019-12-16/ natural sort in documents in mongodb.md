###  natural sort in documents in mongodb


[$natural — MongoDB Manual](https://docs.mongodb.com/manual/reference/operator/meta/natural "$natural — MongoDB Manual")


 

```js
db.getCollection('criticalLog').find({}).sort({$natural:-1})
```
