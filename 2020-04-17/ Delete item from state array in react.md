###  Delete item from state array in react


[javascript - Delete item from state array in react - Stack Overflow](https://stackoverflow.com/questions/36326612/delete-item-from-state-array-in-react "javascript - Delete item from state array in react - Stack Overflow")


 

```js
removePeople(e) {
    this.setState({people: this.state.people.filter(function(person) { 
        return person !== e.target.value 
    })});
}
```
