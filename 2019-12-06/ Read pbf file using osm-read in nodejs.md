###  Read pbf file using osm-read in nodejs





 

```js
var osmread = require("osm-read")
var parser = osmread.parse({
    filePath: 'ULID_443new.pbf',
    endDocument: function(){
        console.log('document end');
    },
    bounds: function(bounds){
        console.log('bounds: ' + JSON.stringify(bounds));
    },
    node: function(node){
        console.log('node: ' + JSON.stringify(node));
    },
    way: function(way){
        console.log('way: ' + JSON.stringify(way));
    },
    relation: function(relation){
        console.log('relation: ' + JSON.stringify(relation));
    },
    error: function(msg){
        console.log('error: ' + msg);
    }
});

```
