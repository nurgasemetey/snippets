###  firestore security rules


[Basic Security Rules | Firebase](https://firebase.google.com/docs/rules/basics?authuser=0 "Basic Security Rules  |  Firebase")







[Basic examples of using Cloud Firestore Security Rules | by Kacper Hreniak | Medium](https://medium.com/@khreniak/advanced-examples-of-using-cloud-firestore-security-rules-9e641d023c7e "Basic examples of using Cloud Firestore Security Rules | by Kacper Hreniak | Medium")







[flutter - Firebase Cloud Database Rules - how to retrieve data only where the user id matches a key in the object? - Stack Overflow](https://stackoverflow.com/questions/61950258/firebase-cloud-database-rules-how-to-retrieve-data-only-where-the-user-id-matc "flutter - Firebase Cloud Database Rules - how to retrieve data only where the user id matches a key in the object? - Stack Overflow")


 

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /decision/{document} {
      allow create: if request.auth.uid == request.resource.data.uid;
      allow read, write, update: if request.auth != null && request.auth.uid == resource.data.uid
    }
    
    match /decisionRate/{document} {
    	allow create: if request.auth.uid == request.resource.data.uid;
      allow read, write, update: if request.auth != null && request.auth.uid == resource.data.uid
    }
  }
}
```
