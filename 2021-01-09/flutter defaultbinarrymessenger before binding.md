### flutter defaultbinarrymessenger before binding


[Flutter: Unhandled Exception: ServicesBinding.defaultBinaryMessenger was accessed before the binding was initialized - Stack Overflow](https://stackoverflow.com/questions/57689492/flutter-unhandled-exception-servicesbinding-defaultbinarymessenger-was-accesse "Flutter: Unhandled Exception: ServicesBinding.defaultBinaryMessenger was accessed before the binding was initialized - Stack Overflow")


 

```

void main() async {
  WidgetsFlutterBinding.ensureInitialized();   //  ADD THIS BEFORE YOUR ASYNC FUNCTION CALL.
  await Firestore.instance.settings(...);      //  NOW YOU CAN CALL ASYNC FUNCTION.   
  ...
  runApp(
    ...
  )
```
