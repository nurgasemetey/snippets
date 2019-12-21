### multiple documents with a single command in mongo


[MongoDB: How to update multiple documents with a single command? - Stack Overflow](https://stackoverflow.com/questions/1740023/mongodb-how-to-update-multiple-documents-with-a-single-command)




```js
db.test.updateMany({foo: "bar"}, {$set: {test: "success!"}})

```
