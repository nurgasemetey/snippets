### query data in sqlite3 in nodejs


[Querying Data in SQLite Database from Node.js Applications](https://www.sqlitetutorial.net/sqlite-nodejs/query/ "Querying Data in SQLite Database from Node.js Applications")




```js
var getDeviceInfo = async function (deviceMac) {

    let sql = `SELECT username username,
        deviceMac deviceMac
        FROM user_info
        WHERE deviceMac  = ?`;
    return new Promise((resolve, reject) => {
        db.get(sql, [deviceMac], (err, row) => {
            if (err) {
                reject(err)
            }
            resolve(row);
        });
    });
}
```
