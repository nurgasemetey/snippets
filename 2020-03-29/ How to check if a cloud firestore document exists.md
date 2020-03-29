###  How to check if a cloud firestore document exists


[javascript - How to check if a cloud firestore document exists when using realtime updates - Stack Overflow](https://stackoverflow.com/questions/46880323/how-to-check-if-a-cloud-firestore-document-exists-when-using-realtime-updates "javascript - How to check if a cloud firestore document exists when using realtime updates - Stack Overflow")


 

```js
const usersRef = db.collection('users').doc('id')

usersRef.get()
  .then((docSnapshot) => {
    if (docSnapshot.exists) {
      usersRef.onSnapshot((doc) => {
        // do stuff with the data
      });
    } else {
      usersRef.set({...}) // create the document
    }
});
```
