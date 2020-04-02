###  How to call loading function with React useEffect only once


[javascript - How to call loading function with React useEffect only once - Stack Overflow](https://stackoverflow.com/questions/53120972/how-to-call-loading-function-with-react-useeffect-only-once "javascript - How to call loading function with React useEffect only once - Stack Overflow")


 

```js
useEffect(yourCallback, []) - will trigger the callback only after the first render.


```
