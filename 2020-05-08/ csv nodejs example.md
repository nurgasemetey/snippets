###  csv nodejs example


[Methods | Fast-CSV](https://c2fo.io/fast-csv/docs/parsing/methods "Methods | Fast-CSV")


 

```js
fs.createReadStream(process.argv[2])
  .pipe(csv.parse({ headers: true }))
  .on('error', error => console.error(error))
  .on('data', row => {
    // console.log(row);
    coordinates.push([parseFloat(row['X']), parseFloat(row['Y'])]);
    timestamps.push(1000);
    radiuses.push(300);
  })
  .on('end', rowCount => {
    // console.log(coordinates);
  });
```
