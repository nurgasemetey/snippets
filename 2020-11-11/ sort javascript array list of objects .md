###  sort javascript array list of objects 


[How to sort an array of objects by a property value in JavaScript](https://flaviocopes.com/how-to-sort-array-of-objects-by-property-javascript/ "How to sort an array of objects by a property value in JavaScript")


 

```
const list = [
  { color: 'white', size: 'XXL' },
  { color: 'red', size: 'XL' },
  { color: 'black', size: 'M' }
]

list.sort((a, b) => (a.color > b.color) ? 1 : -1)

```
