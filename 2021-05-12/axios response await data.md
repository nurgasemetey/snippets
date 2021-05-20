### axios response await data


[javascript - Get response from axios with await/async - Stack Overflow](https://stackoverflow.com/questions/49661209/get-response-from-axios-with-await-async/49661388 "javascript - Get response from axios with await/async - Stack Overflow")


 

```
async function getData() {
    try {
       let res = await axios({
            url: 'https://jsonplaceholder.typicode.com/posts/1',
            method: 'get',
            timeout: 8000,
            headers: {
                'Content-Type': 'application/json',
            }
        })
        if(res.status == 200){
            // test for status you want, etc
            console.log(res.status)
        }    
        // Don't forget to return something   
        return res.data
    }
    catch (err) {
        console.error(err);
    }
}

getData()
.then(res => console.log(res))
```
