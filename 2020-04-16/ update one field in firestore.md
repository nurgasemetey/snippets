###  update one field in firestore

[How to update a single firebase firestore document - Stack Overflow](https://stackoverflow.com/questions/49682327/how-to-update-a-single-firebase-firestore-document "How to update a single firebase firestore document - Stack Overflow")

 

```js
If you want to only update the values of the field you specify in a map, use update():

let result = await db.collection("teams")
            .doc(teamSnapshot.id)
            .update({
              "users": users
            });
```
