###  connect to sqlite3 in nodejs


[Connecting To SQLite Database Using Node.js](https://www.sqlitetutorial.net/sqlite-nodejs/connect/ "Connecting To SQLite Database Using Node.js")


 

```js
let db = new sqlite3.Database('./db/chinook.db', sqlite3.OPEN_READWRITE | sqlite3.OPEN_CREATE, (err) => {
    if (err) {
        console.error(err.message);
    }
    console.log('Connected to the chinook database.');
});
```
