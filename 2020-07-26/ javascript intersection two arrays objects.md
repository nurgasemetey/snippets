###  javascript intersection two arrays objects


[How to find all intersections between two arrays of objects in javascript React? - Stack Overflow](https://stackoverflow.com/questions/57674783/how-to-find-all-intersections-between-two-arrays-of-objects-in-javascript-react "How to find all intersections between two arrays of objects in javascript React? - Stack Overflow")


 

```
let details = [
  {a: 1, b: 200, name: "dad"}, 
  {a:2, b: 250, name: "cat"}, 
  {a:3, b: 212, name: "dog" } 
] 

let certs = [
  {id: 991, b: 250, dn: "qwerty", sign: "GOST"}, 
  {id: 950, b: 251, dn: "how", sign: "RSA" }, 
  {id: 100, b: 250, dn: "how are", sign: "twofish" }, 
  {id: 957, b: 212, dn: "how you", sign: "black" }
] 

const result = certs.filter(cert => {
	let arr = details.filter(detail => detail.b === cert.b)
	return !(arr.length === 0)
});

console.log(result)
```
