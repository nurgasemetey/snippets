### axios delete example 


[javascript - Axios Delete request with body and headers? - Stack Overflow](https://stackoverflow.com/questions/51069552/axios-delete-request-with-body-and-headers "javascript - Axios Delete request with body and headers? - Stack Overflow")


 

```
let config = { 
    headers: {
        Authorization: authToken
    },
    data: { //! Take note of the `data` keyword. This is the request body.
        key: value,
        ... //! more `key: value` pairs as desired.
    } 
}

axios.delete(url, config)
```
