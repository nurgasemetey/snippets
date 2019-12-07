###  Write to a CSV in Node.js


[javascript - Write to a CSV in Node.js - Stack Overflow](https://stackoverflow.com/questions/10227107/write-to-a-csv-in-node-js "javascript - Write to a CSV in Node.js - Stack Overflow")


 

```js
import stringify from 'csv-stringify';
import fs from 'fs';

let data = [];
let columns = {
  id: 'id',
  name: 'Name'
};

for (var i = 0; i < 10; i++) {
  data.push([i, 'Name ' + i]);
}

stringify(data, { header: true, columns: columns }, (err, output) => {
  if (err) throw err;
  fs.writeFile('my.csv', output, (err) => {
    if (err) throw err;
    console.log('my.csv saved.');
  });
});
```
