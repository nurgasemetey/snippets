###  util helper typescript


[typescript - How to structure utility class - Stack Overflow](https://stackoverflow.com/questions/32790311/how-to-structure-utility-class "typescript - How to structure utility class - Stack Overflow")


 

```ts
export default class Utils {
    static doSomething(val: string) { return val; }
    static doSomethingElse(val: string) { return val; }
}

import Utils from './utils'

export class MyClass {
     constructor()
     {
         Utils.doSomething("test");
     }
}
```
