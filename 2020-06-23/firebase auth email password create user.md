### firebase auth email password create user


[Authenticate with Firebase using Password-Based Accounts using Javascript](https://firebase.google.com/docs/auth "Authenticate with Firebase using Password-Based Accounts using Javascript")


 

```js
firebase.auth().createUserWithEmailAndPassword(email, password).catch(function(error) {
  // Handle Errors here.
  var errorCode = error.code;
  var errorMessage = error.message;
  // ...
});
```
