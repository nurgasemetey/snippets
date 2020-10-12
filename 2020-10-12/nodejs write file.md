### nodejs write file


[Node.js | fs.writeFileSync() Method - GeeksforGeeks](https://www.geeksforgeeks.org/node-js-fs-writefilesync-method/ "Node.js | fs.writeFileSync() Method - GeeksforGeeks")


 

```
const fs = require('fs'); 
  
let data = "This is a file containing a collection"
           + " of programming languages.\n"
 + "1. C\n2. C++\n3. Python"; 
  
fs.writeFileSync("programming.txt", data); 
```
