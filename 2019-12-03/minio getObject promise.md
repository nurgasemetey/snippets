###  minio getObject promise


[s3.getObject Promise example · Issue #1436 · aws/aws-sdk-js](https://github.com/aws/aws-sdk-js/issues/1436 "s3.getObject Promise example · Issue #1436 · aws/aws-sdk-js")


 

```javascript
  const getObject = (handle) => {
    return new Promise((resolve, reject) => {
      s3.getObject(handle, (err, data) => {
        if (err) reject(err)
        else resolve(data.Body)
      })
    })
  };
```
