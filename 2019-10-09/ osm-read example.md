###  osm-read example


[marook/osm-read: an openstreetmap XML and PBF data parser for node.js and the browser](https://github.com/marook/osm-read)


 

```js
var osmread = require("osm-read")
var parser = osmread.parse({
    filePath: 'ulid443_station2_01.pbf',
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
