###  flutter application launcher


[dart - How to change the application launcher icon on Flutter? - Stack Overflow](https://stackoverflow.com/questions/43928702/how-to-change-the-application-launcher-icon-on-flutter/52829977#52829977 "dart - How to change the application launcher icon on Flutter? - Stack Overflow")


 

```
dev_dependencies:
  flutter_launcher_icons: 0.8.1
  flutter_test:
    sdk: flutter

# For information on the generic Dart part of this file, see the
# following page: https://dart.dev/tools/pub/pubspec

flutter_icons:
  android: true
  ios: true
  image_path: "icon/icon.png"

---

$ flutter pub get

$ flutter pub run flutter_launcher_icons:main


```
