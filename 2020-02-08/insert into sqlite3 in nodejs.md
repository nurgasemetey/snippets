### insert into sqlite3 in nodejs


[Inserting Data Into an SQLite Table from a Node.js Application](https://www.sqlitetutorial.net/sqlite-nodejs/insert/ "Inserting Data Into an SQLite Table from a Node.js Application")




```js
db.run(`INSERT INTO user_info(username, deviceMac) VALUES(?, ?)`, [deviceRegistrationInfo.username, deviceRegistrationInfo.deviceMac], function (err) {
        if (err) {
            console.log("error: ", err.message);
            res.send({ username: os.userInfo().username })
            return;
        }
        // get the last insert id
        console.log(`A row has been inserted with rowid ${this.lastID}`);
        res.send({ username: os.userInfo().username })
    });
```
