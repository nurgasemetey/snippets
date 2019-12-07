###  Cannot read property 'props' of undefined


[javascript - React - TypeError: Cannot read property 'props' of undefined - Stack Overflow](https://stackoverflow.com/questions/50862192/react-typeerror-cannot-read-property-props-of-undefined "javascript - React - TypeError: Cannot read property 'props' of undefined - Stack Overflow")


 

```js
class Character extends Component {
    render() {
        // ...
    };

    handleDelete = () => {
        this.props.onDelete(this.props.char);
    }
}
```
