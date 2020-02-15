### promise resolve in async function


[Async JavaScript: From Callbacks, to Promises, to Async/Await](https://tylermcginnis.com/async-javascript-from-callbacks-to-promises-to-async-await/ "Async JavaScript: From Callbacks, to Promises, to Async/Await")




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
