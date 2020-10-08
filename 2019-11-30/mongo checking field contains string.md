### mongo checking field contains string


[mongodb - Checking if a field contains a string - Stack Overflow](https://stackoverflow.com/questions/10610131/checking-if-a-field-contains-a-string "mongodb - Checking if a field contains a string - Stack Overflow")


 

```js
db.users.findOne({"username" : {$regex : ".*son.*"}});

```
