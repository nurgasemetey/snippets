### last records in mongodb


[How to get the last N records in mongodb? - Stack Overflow](https://stackoverflow.com/questions/4421207/how-to-get-the-last-n-records-in-mongodb)




```js
db.foo.find().sort({_id:1}).limit(50);

```
