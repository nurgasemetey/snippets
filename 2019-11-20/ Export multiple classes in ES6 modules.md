###  Export multiple classes in ES6 modules


[javascript - Export multiple classes in ES6 modules - Stack Overflow](https://stackoverflow.com/questions/38340500/export-multiple-classes-in-es6-modules "javascript - Export multiple classes in ES6 modules - Stack Overflow")


 

```js
export const MyFunction = () => {}
export const MyFunction2 = () => {}

const Var = 1;
const Var2 = 2;

export {
   Var,
   Var2,
}


// Then import it this way
import {
  MyFunction,
  MyFunction2,
  Var,
  Var2,
} fr
```
