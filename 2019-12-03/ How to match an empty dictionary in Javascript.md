###  How to match an empty dictionary in Javascript


[How to match an empty dictionary in Javascript? - Stack Overflow](https://stackoverflow.com/questions/6072590/how-to-match-an-empty-dictionary-in-javascript "How to match an empty dictionary in Javascript? - Stack Overflow")


 

```js
function isEmpty(obj) {
  return Object.keys(obj).length === 0;
}
```
