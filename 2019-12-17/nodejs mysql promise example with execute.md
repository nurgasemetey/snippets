### nodejs mysql promise example with execute


[sidorares/node-mysql2: fast node-mysql compatible mysql driver for node.js](https://github.com/sidorares/node-mysql2 "sidorares/node-mysql2: fast node-mysql compatible mysql driver for node.js")




```js
async function main() {
  // get the client
  const mysql = require('mysql2/promise');
  // create the connection
  const connection = await mysql.createConnection({host:'localhost', user: 'root', database: 'test'});
  // query database
  const [rows, fields] = await connection.execute('SELECT * FROM `table` WHERE `name` = ? AND `age` > ?', ['Morty', 14]);
}
```
