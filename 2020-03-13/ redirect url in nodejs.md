###  redirect url in nodejs


[node.js - Nodejs - Redirect url - Stack Overflow](https://stackoverflow.com/questions/4062260/nodejs-redirect-url "node.js - Nodejs - Redirect url - Stack Overflow")


 

```js
response.writeHead(302, {
  'Location': 'your/404/path.html'
  //add other headers here...
});
response.end();
```
