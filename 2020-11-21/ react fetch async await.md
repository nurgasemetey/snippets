###  react fetch async await


[How To Use Async Await in React (componentDidMount Async)](https://www.valentinog.com/blog/await-react/ "How To Use Async Await in React (componentDidMount Async)")


 

```
async componentDidMount() {
    const response = await fetch(`https://api.coinmarketcap.com/v1/ticker/?limit=10`);
    const json = await response.json();
    this.setState({ data: json });
  }
```
