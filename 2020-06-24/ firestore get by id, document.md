###  firestore get by id, document


[Get data with Cloud Firestore | Firebase](https://firebase.google.com/docs/firestore/query-data/get-data "Get data with Cloud Firestore  |  Firebase")


 

```js
var docRef = db.collection("cities").doc("SF");

docRef.get().then(function(doc) {
    if (doc.exists) {
        console.log("Document data:", doc.data());
    } else {
        // doc.data() will be undefined in this case
        console.log("No such document!");
    }
}).catch(function(error) {
    console.log("Error getting document:", error);
});


---

const db = app.firestore();
            let query = await db.collection('company').doc(companyId)
                .get();
            console.log(query);
            if(query.exists) {
                let obj:any = query.data()
                console.log(obj);
                let companyName = obj["companyName"];
                this.setState({ companyName:  companyName});

            }
```
