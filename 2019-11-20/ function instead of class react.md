###  function instead of class react


[reactjs - create-react-app generates function instead of class in App.js - Stack Overflow](https://stackoverflow.com/questions/56297983/create-react-app-generates-function-instead-of-class-in-app-js "reactjs - create-react-app generates function instead of class in App.js - Stack Overflow")


 

```js
import React, {Component} from 'react';
import logo from './logo.svg';
import './App.css';

class App extends Component {
  render() {
    return (
      <div className="App">
        <header className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <p>
            Edit <code>src/App.js</code> and save to reload.
          </p>
          <a
            className="App-link"
            href="https://reactjs.org"
            target="_blank"
            rel="noopener noreferrer"
          >
            Learn React
          </a>
        </header>
      </div>
    );
  }
}
export default App;

```
