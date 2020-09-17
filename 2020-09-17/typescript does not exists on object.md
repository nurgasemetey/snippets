### typescript does not exists on object


[typescript - Property does not exist on type 'object' - Stack Overflow](https://stackoverflow.com/questions/43338763/property-does-not-exist-on-type-object "typescript - Property does not exist on type 'object' - Stack Overflow")




```
You probably have allProviders typed as object[] as well. And property country does not exist on object. If you don't care about typing, you can declare both allProviders and countryProviders as Array<any>:

let countryProviders: Array<any>;
let allProviders: Array<any>;
```
