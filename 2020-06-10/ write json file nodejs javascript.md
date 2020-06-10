###  write json file nodejs javascript


[Reading and Writing JSON Files with Node.js](https://stackabuse.com/reading-and-writing-json-files-with-node-js/ "Reading and Writing JSON Files with Node.js")


 

```js

const fs = require('fs');

let student = { 
    name: 'Mike',
    age: 23, 
    gender: 'Male',
    department: 'English',
    car: 'Honda' 
};
 
let data = JSON.stringify(student);
fs.writeFileSync('student-2.json', data);
```
