###  firebase send email verification


[firebase - get notified when user confirmed an email sent with sendEmailVerification - Stack Overflow](https://stackoverflow.com/questions/37912615/firebase-get-notified-when-user-confirmed-an-email-sent-with-sendemailverifica "firebase - get notified when user confirmed an email sent with sendEmailVerification - Stack Overflow")


 

```ts
await app
                .auth()
                .createUserWithEmailAndPassword(values.email, values.password);
            let user = app.auth().currentUser;
            await user.sendEmailVerification();

            await user.updateProfile({
                    displayName: values.nameSurname,
                  });
            setLoading(f
```
