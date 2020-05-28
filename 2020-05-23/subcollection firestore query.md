### subcollection firestore query


[Perform simple and compound queries in Cloud Firestore | Firebase](https://firebase.google.com/docs/firestore/query-data/queries#web_13 "Perform simple and compound queries in Cloud Firestore  |  Firebase")




```
var museums = db.collectionGroup('landmarks').where('type', '==', 'museum');
let itemMoodsRef = await db.collectionGroup('comments')
        .where('email', '==', 'keke@keke.com') //TODO real username
        .get();
```
