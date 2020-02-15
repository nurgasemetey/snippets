### post example using fetch


[javascript - Fetch: POST json data - Stack Overflow](https://stackoverflow.com/questions/29775797/fetch-post-json-data "javascript - Fetch: POST json data - Stack Overflow")


 

```js
fetch('http://localhost:8080/api/registerDevice', {
                                    method: 'post',
                                    headers: {
                                        'Accept': 'application/json, text/plain, */*',
                                        'Content-Type': 'application/json'
                                    },
                                    body: JSON.stringify({
                                        username: this.state.username,
                                        deviceMac: this.props.device.mac
                                    })
                                }).then(function (response) {
                                    return response.json();
                                }).then(function (data) {
                                    console.log(data);
                                    console.log("registered");
                                }).catch(function (error) {
                                    console.log(error);
                                });
```
