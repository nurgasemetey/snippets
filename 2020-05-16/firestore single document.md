### firestore single document


[Read a Single Firestore Document](https://fireship.io/snippets/read-a-single-firestore-document/ "Read a Single Firestore Document")


 

```
async function getUserByEmail(email) {
  // Make the initial query
  const query = await db.collection('users').where('email', '==', email).get();

   if (!result.empty) {
    const snapshot = query.docs[0];
    const data = snapshot.data();
  } else {
    // not found
  }

}
```
