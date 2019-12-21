###  nodejs limit entity size


[javascript - Error: request entity too large - Stack Overflow](https://stackoverflow.com/questions/19917401/error-request-entity-too-large)


 

```js
app.use(bodyParser.json({limit: '50mb'}));

```
