###  update display name firebase auth


[Manage Users in Firebase](https://firebase.google.com/docs/auth/web/manage-users#update_a_users_profile "Manage Users in Firebase")


 

```
var user = firebase.auth().currentUser;

user.updateProfile({
  displayName: "Jane Q. User",
  photoURL: "https://example.com/jane-q-user/profile.jpg"
}).then(function() {
  // Update successful.
}).catch(function(error) {
  // An error happened.
});
```
