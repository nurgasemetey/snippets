### How do I remove a key from a JavaScript object


[How do I remove a key from a JavaScript object? - Stack Overflow](https://stackoverflow.com/questions/3455405/how-do-i-remove-a-key-from-a-javascript-object "How do I remove a key from a JavaScript object? - Stack Overflow")




```js
delete thisIsObject['Cow'];

//with lodash
var thisIsObject= {
    'Cow' : 'Moo',
    'Cat' : 'Meow',
    'Dog' : 'Bark'
};
_.omit(thisIsObject,'Cow'); //It will return a new object

=> {'Cat' : 'Meow', 'Dog' : 'Bark'}  //resu
```
