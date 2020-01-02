### date query in mongo 


[json - Date query with ISODate in mongodb doesn't seem to work - Stack Overflow](https://stackoverflow.com/questions/19819870/date-query-with-isodate-in-mongodb-doesnt-seem-to-work "json - Date query with ISODate in mongodb doesn't seem to work - Stack Overflow")


 

```js
db.mycollection.find({
    "dt" : {"$gte": ISODate("2013-10-01T00:00:00.000Z")}
})
```
