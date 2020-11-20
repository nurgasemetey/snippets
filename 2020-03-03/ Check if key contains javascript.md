###  Check if key contains javascript



[arrays - Checking if a key exists in a JavaScript object? - Stack Overflow](https://stackoverflow.com/questions/1098040/checking-if-a-key-exists-in-a-javascript-object "arrays - Checking if a key exists in a JavaScript object? - Stack Overflow")


 

```javascript
!("key" in obj) // true if "key" doesn't exist in object
!"key" in obj   // ERROR!  Equivalent to "false in obj"
```
