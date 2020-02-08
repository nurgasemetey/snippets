### express json endpoint post request


[node.js - How do I consume the JSON POST data in an Express application - Stack Overflow](https://stackoverflow.com/questions/10005939/how-do-i-consume-the-json-post-data-in-an-express-application "node.js - How do I consume the JSON POST data in an Express application - Stack Overflow")




```js
var express = require('express');

var app = express();

app.use(express.json());

app.post('/', function(request, response){
  console.log(request.body);      // your JSON
   response.send(request.body);    // echo the result back
});

app.listen(3000);
```
