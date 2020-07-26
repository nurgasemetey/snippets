### javascript array to dictionary map


[JavaScript: Map an array of objects to a dictionary - DEV](https://dev.to/devtronic/javascript-map-an-array-of-objects-to-a-dictionary-3f42 "JavaScript: Map an array of objects to a dictionary - DEV")


 

```
let data = [
  {id: 1, country: 'Germany', population: 83623528},
  {id: 2, country: 'Austria', population: 8975552},
  {id: 3, country: 'Switzerland', population: 8616571}
];

let dictionary = Object.assign({}, ...data.map((x) => ({[x.id]: x.country})));

```
