### list to map javascript 


[javascript - Convert object array to hash map, indexed by an attribute value of the Object - Stack Overflow](https://stackoverflow.com/questions/26264956/convert-object-array-to-hash-map-indexed-by-an-attribute-value-of-the-object "javascript - Convert object array to hash map, indexed by an attribute value of the Object - Stack Overflow")


 

```
const hash = Object.assign({}, ...array.map(s => ({[s.key]: s.value})));

```
