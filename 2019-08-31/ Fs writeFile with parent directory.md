###  Fs writeFile with parent directory


[node.js - How to write file if parent folder doesn't exist? - Stack Overflow](https://stackoverflow.com/questions/16316330/how-to-write-file-if-parent-folder-doesnt-exist)


 Creating parent if not exists while write file

```js
var fs = require('fs-extra');
var file = '/tmp/this/path/does/not/exist/file.txt'

fs.outputFile(file, 'hello!', function (err) {
    console.log(err); // => null

    fs.readFile(file, 'utf8', function (err, data) {
        console.log(data); // => hello!
    });
});

```
