###  react router typescript match params


[reactjs - react-router-dom with TypeScript - Stack Overflow](https://stackoverflow.com/questions/44118060/react-router-dom-with-typescript "reactjs - react-router-dom with TypeScript - Stack Overflow")


 

```
interface HomeRouterProps {
  title: string;   // This one is coming from the router
}

interface HomeProps extends RouteComponentProps<HomeRouterProps> {
  // Add your regular properties here
}

interface HomeDispatchProps {
  // Add your dispatcher properties here
}


class Home extends React.Component<HomeProps & HomeDispatchProps> {
  constructor(props: HomeProps & HomeDispatchProps) {
    super(props);
  }

  public render() {
    return (<span>{this.props.match.params.title}</span>);
  }
}
```
