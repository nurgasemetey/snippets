### nodejs synchronous request


[node.js - Convert a JSON Object to Buffer and Buffer to JSON Object back - Stack Overflow](https://stackoverflow.com/questions/41951307/convert-a-json-object-to-buffer-and-buffer-to-json-object-back "node.js - Convert a JSON Object to Buffer and Buffer to JSON Object back - Stack Overflow")





[javascript - Synchronous Requests in Node.js - Stack Overflow](https://stackoverflow.com/questions/8775262/synchronous-requests-in-node-js "javascript - Synchronous Requests in Node.js - Stack Overflow")




```
var request = require('sync-request');
var res = request('GET', 'http://example.com');
console.log(res.getBody()); //buffer

let response = JSON.parse(res.getBody().toString());

```
