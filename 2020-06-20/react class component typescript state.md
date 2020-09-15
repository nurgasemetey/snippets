###  react class component typescript state


[javascript - Using state in react with TypeScript - Stack Overflow](https://stackoverflow.com/questions/46987816/using-state-in-react-with-typescript "javascript - Using state in react with TypeScript - Stack Overflow")

[TypeScript and React: Components](https://fettblog.eu/typescript-react/components/ "TypeScript and React: Components")
 

```js
interface IProps {
}

interface IState {
  playOrPause?: string;
}

class Player extends React.Component<IProps, IState> {
  // ------------------------------------------^
  constructor(props: IProps) {
    super(props);

    this.state = {
      playOrPause: 'Play'
    };
  }

  render() {
    return(
      <div>
        <button
          ref={playPause => this.playPause = playPause}
          title={this.state.playOrPause} // in this line I get an error
        >
          Play
        </button>
      </div>
    );
  }
}
```
