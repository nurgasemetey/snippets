### how to pass function to child component 


[reactjs - React Pass function to child component - Stack Overflow](https://stackoverflow.com/questions/48407785/react-pass-function-to-child-component "reactjs - React Pass function to child component - Stack Overflow")


 

```js
class Child extends Component {
    render() {
        <div onClick={this.props.passedFunction}></div>
    }
}

class Parent extends Component {
    passedFunction = () => {}
    render() {
      <Child passedFunction={this.passedFunction}/>
    }
}
```
