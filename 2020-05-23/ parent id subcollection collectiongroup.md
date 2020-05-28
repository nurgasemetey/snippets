###  parent id subcollection collectiongroup


[android - Firestore - get the parent document of a subcollection - Stack Overflow](https://stackoverflow.com/questions/56219469/firestore-get-the-parent-document-of-a-subcollection "android - Firestore - get the parent document of a subcollection - Stack Overflow")


 

```
await db.collection('moods').doc(comment.ref.parent.parent.id).get();
```
