###  Async in array iteration in typescript

[promise - Simplify async-await with array iteration in Typescript - Stack Overflow](https://stackoverflow.com/questions/50377665/simplify-async-await-with-array-iteration-in-typescript "promise - Simplify async-await with array iteration in Typescript - Stack Overflow")




```js
for (const item of items) {
    doSomething(item);
    const result = await doSomethingAsync(item);
    doSomethingMore(result, item);
});

```

