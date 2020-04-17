### How to get document id after adding a document to a collection


[firebase - Firestore - How to get document id after adding a document to a collection - Stack Overflow](https://stackoverflow.com/questions/48740430/firestore-how-to-get-document-id-after-adding-a-document-to-a-collection "firebase - Firestore - How to get document id after adding a document to a collection - Stack Overflow")




```js
// Add a new document with a generated id.
db.collection("cities").add({
    name: "Tokyo",
    country: "Japan"
})
.then(function(docRef) {
    console.log("Document written with ID: ", docRef.id);
})
.catch(function(error) {
    console.error("Error adding document: ", error);
});
```
