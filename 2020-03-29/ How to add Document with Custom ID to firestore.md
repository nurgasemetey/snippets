###  How to add Document with Custom ID to firestore


[javascript - How to add Document with Custom ID to firestore - Stack Overflow](https://stackoverflow.com/questions/48541270/how-to-add-document-with-custom-id-to-firestore "javascript - How to add Document with Custom ID to firestore - Stack Overflow")


 

```js
db.collection("cities").doc("LA").set({
    name: "Los Angeles",
    state: "CA",
    country: "USA"
})
```
