### generate every minutes day 


https://stackoverflow.com/a/36134998/1780700

[Generate array of times (as strings) for every X minutes in JavaScript - Stack Overflow](https://stackoverflow.com/questions/36125038/generate-array-of-times-as-strings-for-every-x-minutes-in-javascript "Generate array of times (as strings) for every X minutes in JavaScript - Stack Overflow")


 

```js
  const generateLoopData = name => {
    const dt = new Date(1970, 0, 1);
    const rc = [];
    while (dt.getDate() === 1) {
      let hour = dt.toLocaleTimeString('en-GB', {
        hour: '2-digit',
        minute: '2-digit',
        hour12: false,
      });
      rc.push({
        name: hour,
        [`${name}_value`]: Math.floor(Math.random() * 100),
      });
      dt.setMinutes(dt.getMinutes() + 180);
    }
    return rc;
  };
```
