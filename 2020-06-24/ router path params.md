###  router path params


[javascript - Get path params in react-router v4 - Stack Overflow](https://stackoverflow.com/questions/45468837/get-path-params-in-react-router-v4 "javascript - Get path params in react-router v4 - Stack Overflow")


 

```ts
      <Router>
        <PrivateRoute path="/" exact={true} component={TodosContainer} />
        <Route exact path="/login" component={Login} />
        <Route exact path="/public/company/:companyId" render={({match}) => (<PublicView companyId={match.params.companyId}/>)}/>

      </Router>
```
