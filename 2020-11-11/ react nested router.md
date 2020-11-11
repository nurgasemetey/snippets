###  react nested router


[javascript - Nested routes with react router v4 / v5 - Stack Overflow](https://stackoverflow.com/questions/41474134/nested-routes-with-react-router-v4-v5?answertab=oldest#tab-top "javascript - Nested routes with react router v4 / v5 - Stack Overflow")


 

```
<BrowserRouter>
  <Switch>
    <Route path="/staffs/:id/edit" component={StaffEdit} />
    <Route path="/staffs/:id" component={StaffShow} />
    <Route path="/staffs" component={StaffIndex} />
  </Switch>
</BrowserRouter>
```
