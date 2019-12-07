###  Passing data between two sibling React.js components


[javascript - Passing data between two sibling React.js components - Stack Overflow](https://stackoverflow.com/questions/34734301/passing-data-between-two-sibling-react-js-components "javascript - Passing data between two sibling React.js components - Stack Overflow")


 

```js
class Parent extends React.Component {
    constructor(props) {
        super(props);
        this.state = {shared_var: "init"};
    }

    updateShared(shared_value) {
        this.setState({shared_var: shared_value});
    }

    render() {
        return (
            <div>
                <CardSearch shared_var={this.state.shared_var} updateShared={this.updateShared} />
                <RunOnServer shared_var={this.state.shared_var} updateShared={this.updateShared} />
                <div> The shared value is {this.state.shared_var} </div>
            </div>
        );
    }
}

class CardSearch extends React.Component {
    updateShared() {
        this.props.updateShared('card');
    }

    render() {
        return (
            <button onClick={this.updateShared} style={this.props.shared_var == 'card' ? {backgroundColor: "green"} : null} >
            card
            </button>
        );
    }
}

class RunOnServer extends React.Component {
    updateShared() {
        this.props.updateShared('run');
    }

    render() {
        return (
            <button onClick={this.updateShared} style={this.props.shared_var == 'run' ? {backgroundColor: "green"} : null}>
            run
            </button>
        );
    }
}


ReactDOM.render(
  <Parent/>,
  document.getElementById('container')
);
```
