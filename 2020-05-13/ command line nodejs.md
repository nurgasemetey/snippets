###  command line nodejs


[minimist - npm](https://www.npmjs.com/package/minimist "minimist - npm")

[Node, accept arguments from the command line](https://flaviocopes.com/node-cli-args/ "Node, accept arguments from the command line")


 

```js
let argv = require('minimist')(process.argv.slice(2));
  console.log(argv)
  if(argv["swagger-generate"]) {
    fs.writeFileSync("./swagger-spec.json", JSON.stringify(document));
    process.exit(0);
  }


node dist/main --swagger-generate=True
```
