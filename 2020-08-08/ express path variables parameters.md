###  express path variables parameters


[Express routing](https://expressjs.com/en/guide/routing.html "Express routing")


 

```
app.get('/users/:userId/books/:bookId', function (req, res) {
  res.send(req.params)
})
```
