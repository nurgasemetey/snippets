###  firebase firestore date query


[firebase - Firestore query by date range - Stack Overflow](https://stackoverflow.com/questions/47000854/firestore-query-by-date-range "firebase - Firestore query by date range - Stack Overflow")


 

```js
const event = new Date();
const expirationDate = admin.firestore.Timestamp.fromDate(event);
const query = collectionRef.where('startTime', '<=', expirationDate)

```
