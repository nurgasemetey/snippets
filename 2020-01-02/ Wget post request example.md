###  Wget post request example


[linux - How to do HTTP-request/call with JSON payload from command-line? - Stack Overflow](https://stackoverflow.com/questions/4315111/how-to-do-http-request-call-with-json-payload-from-command-line "linux - How to do HTTP-request/call with JSON payload from command-line? - Stack Overflow")


 

```
wget -O- \
--post-data "grant_type=client_credentials" \
--header="Content-Type: application/x-www-form-urlencoded" \
--header="Authorization: Basic dGVzdF9taWNyb3NlcnZpY2VfY2xpZW50OnRlc3RfbWljcm9zZXJ2aWNlX2NsaWVudF9zZWNyZXQ=" \
'http://auth-server:5002/uaa/oauth/token'


wget --header='Authorization: Bearer 415e61bb-6f9a-45e3-80d3-a126327f410e' 'http://auth-server:5002/uaa/users/byMultipleUsers?username=kuray'
```
