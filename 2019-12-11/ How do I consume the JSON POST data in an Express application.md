###  How do I consume the JSON POST data in an Express application


[node.js - How do I consume the JSON POST data in an Express application - Stack Overflow](https://stackoverflow.com/questions/10005939/how-do-i-consume-the-json-post-data-in-an-express-application "node.js - How do I consume the JSON POST data in an Express application - Stack Overflow")


 

```js
var express    = require('express')
var bodyParser = require('body-parser')

var app = express()

// parse application/json
app.use(bodyParser.json())

app.use(function (req, res, next) {
  console.log(req.body) // populated!
  next()
})

```
