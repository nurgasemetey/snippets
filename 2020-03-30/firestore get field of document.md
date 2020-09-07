###  firestore get field of document





 

```js
let doc = await db.collection("user_ratings").doc(oldDocId).get();
                    if(doc.exists) {
                        console.log("diff: old doc exists");
                        console.log(doc.get("player_count"));
```
