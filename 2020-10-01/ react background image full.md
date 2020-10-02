###  react background image full


[Set background image to full screen in Reactjs - Stack Overflow](https://stackoverflow.com/questions/48288176/set-background-image-to-full-screen-in-reactjs/50769188 "Set background image to full screen in Reactjs - Stack Overflow")


 

```
const styles = {
    container: {
        backgroundImage: `url(${backgroundImage})`,
        backgroundPosition: 'center',
        backgroundSize: 'cover',
        backgroundRepeat: 'no-repeat',
        width: '100vw',
        height: '100vh'
    }
};
```
