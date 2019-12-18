###  throw error in an async function


[javascript - Can I throw error in an async function? - Stack Overflow](https://stackoverflow.com/questions/44562426/can-i-throw-error-in-an-async-function "javascript - Can I throw error in an async function? - Stack Overflow")


 

```js
async function asyncFunc() {
  try {
    await somePromise();
  } catch (error) {
    throw new Error(error);
  }
}
```
