### typescript interface initialize


[oop - typescript interface initialization - Stack Overflow](https://stackoverflow.com/questions/23412033/typescript-interface-initialization "oop - typescript interface initialization - Stack Overflow")


 

```js
interface ISimpleObject {
    foo: string;
    bar?: any;
}

function start(config: ISimpleObject):void {

}

// matches the interface as there is a foo property
start({foo: 'hello'});

// Type assertion -- intellisense will "know" that this is an ISimpleObject
// but it's not necessary as shown above to assert the type
var x = <ISimpleObject> { foo: 'hello' }; 
start(x);

// the type was inferred by declaration of variable type
var x : ISimpleObject = { foo: 'hello' };  
start(x);

// the signature matches ... intellisense won't treat the variable x
// as anything but an object with a property of foo. 
var x = { foo: 'hello' };
start(x);    

// and a class option:
class Simple implements ISimpleObject {
    constructor (public foo: string, public bar?: any) {
       // automatically creates properties for foo and bar
    }
}
start(new Simple("hello"));
```
