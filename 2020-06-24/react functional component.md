### react functional component


[React Function Components - RWieruch](https://www.robinwieruch.de/react-function-component#react-arrow-function-component "React Function Components - RWieruch")




```js
import React from 'react';
 
const App = () => {
  const greeting = 'Hello Function Component!';
 
  return <Headline value={greeting} />;
};
 
const Headline = ({ value }) => {
  return <h1>{value}</h1>;
};
 
export default App;
```
