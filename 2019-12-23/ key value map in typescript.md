###  key value map in typescript


[Is key-value pair available in Typescript? - Stack Overflow](https://stackoverflow.com/questions/36467469/is-key-value-pair-available-in-typescript/50986435)


 

```ts
let yourVar: Map<YourKeyType, YourValueType>;
// now you can use it:
yourVar = new Map<YourKeyType, YourValueType>();
yourVar[YourKeyType] = <YourValueType> yourValue;

```
