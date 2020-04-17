### react arrow without bind


[This is why we need to bind event handlers in Class Components in React](https://www.freecodecamp.org/news/this-is-why-we-need-to-bind-event-handlers-in-class-components-in-react-f7ea1a6f93eb/ "This is why we need to bind event handlers in Class Components in React")


 

```js
class Foo extends React.Component{
 handleClick(event){
    console.log(this);
  }
 
  render(){
    return (
      <button type="button" onClick={(e) => this.handleClick(e)}>
        Click Me
      </button>
    );
  }
}

ReactDOM.render(
  <Foo />,
  document.getElementById("app")
);
```
