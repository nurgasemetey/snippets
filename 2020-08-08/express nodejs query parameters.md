### express nodejs query parameters


[Get Query Strings and Parameters in Express.js](https://stackabuse.com/get-query-strings-and-parameters-in-express-js/ "Get Query Strings and Parameters in Express.js")




```
// Function to handle the root path
app.get('/', async function(req, res) {

    // Access the provided 'page' and 'limt' query parameters
    let page = req.query.page;
    let limit = req.query.limit;
```
