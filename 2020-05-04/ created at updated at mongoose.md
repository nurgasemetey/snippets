###  created at updated at mongoose


[node.js - add created_at and updated_at fields to mongoose schemas - Stack Overflow](https://stackoverflow.com/questions/12669615/add-created-at-and-updated-at-fields-to-mongoose-schemas "node.js - add created_at and updated_at fields to mongoose schemas - Stack Overflow")


 

```js
var UserSchema = new Schema({
    email: String,
    views: { type: Number, default: 0 },
    status: Boolean
}, { timestamps: {} });
```
