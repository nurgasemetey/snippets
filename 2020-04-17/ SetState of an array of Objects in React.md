###  SetState of an array of Objects in React


[reactjs - SetState of an array of Objects in React - Stack Overflow](https://stackoverflow.com/questions/49477547/setstate-of-an-array-of-objects-in-react "reactjs - SetState of an array of Objects in React - Stack Overflow")


 

```js
this.setState(prevState => ({
    itemList: prevState.itemList.map(
    obj => (obj._id === 1234 ? Object.assign(obj, { description: "New Description" }) : obj)
  )
}));
```
