###  android studio dart sdk not configured


[android studio - Dart SDK is not configured - Stack Overflow](https://stackoverflow.com/questions/48650831/dart-sdk-is-not-configured "android studio - Dart SDK is not configured - Stack Overflow")


 

```
File-> Settings (ctrl+alt+s)
Languages and Frameworks -> Dart
Check "Enable Dart support for the project..."
In "Dart SDK path" click in "..." and navigate to flutter SDK directory. Under that directory you'll find "bin/cache/dart-sdk". This is the dart sdk path you should use.
Click "Apply"
Close the project and open it again (sometimes you need this step, sometimes doesn't)
```
