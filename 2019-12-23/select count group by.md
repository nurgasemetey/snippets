### select count group by


[MongoDB SELECT COUNT GROUP BY - Stack Overflow](https://stackoverflow.com/questions/23116330/mongodb-select-count-group-by)




```js
db.contest.aggregate([
    {"$group" : {_id:"$province", count:{$sum:1}}}
])
```
