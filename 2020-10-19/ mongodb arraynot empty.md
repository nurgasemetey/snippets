###  mongodb arraynot empty


[mongoose - Find MongoDB records where array field is not empty - Stack Overflow](https://stackoverflow.com/questions/14789684/find-mongodb-records-where-array-field-is-not-empty "mongoose - Find MongoDB records where array field is not empty - Stack Overflow")


 

```
ME.find({ pictures: { $exists: true, $ne: [] } })

```
