###  Pass data from middleware nodejs


[Express 4.x - API Reference](http://expressjs.com/en/api.html#res.locals)


  Pass data from middleware nodejs

```js
app.use(function (req, res, next) {
  res.locals.user = req.user
  res.locals.authenticated = !req.user.anonymous
  next()
})
```
