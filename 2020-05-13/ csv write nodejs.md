###  csv write nodejs


[Row Types | Fast-CSV](https://c2fo.io/fast-csv/docs/formatting/row-types/ "Row Types | Fast-CSV")


 

```js
var write = async function (data) {

  return new Promise((resolve, reject) => {

    writeToPath('assigned.csv', data,{ headers: true })
      .on('error', err => reject(err))
      .on('finish', () => resolve());
  });

}
```
