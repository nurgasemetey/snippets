###  remove all mongo nodejs


[node.js - nodejs/mongodb, remove entire collection - Stack Overflow](https://stackoverflow.com/questions/8041348/nodejs-mongodb-remove-entire-collection "node.js - nodejs/mongodb, remove entire collection - Stack Overflow")


 

```js
store.collection('sessions',function(err, collection){
    collection.remove({},function(err, removed){
    });
});
```
