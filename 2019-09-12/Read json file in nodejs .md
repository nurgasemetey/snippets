### Read json file in nodejs 


[Reading and Writing JSON Files with Node.js](https://stackabuse.com/reading-and-writing-json-files-with-node-js/)




```js
const fs = require('fs');

let rawdata = fs.readFileSync('student.json');
let docs = JSON.parse(rawdata);
console.log(docs);


---

let docs = require('./student.json');

```
