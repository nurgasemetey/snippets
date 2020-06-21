###  react document title


[javascript - How do you set the document title in React? - Stack Overflow](https://stackoverflow.com/questions/46160461/how-do-you-set-the-document-title-in-react "javascript - How do you set the document title in React? - Stack Overflow")


 

```js
import React from 'react'
import { Helmet } from 'react-helmet'

const TITLE = 'My Page Title'

class MyComponent extends React.PureComponent {
  render () {
    return (
      <>
        <Helmet>
          <title>{ TITLE }</title>
        </Helmet>
        ...
      </>
    )
  }
}
```
