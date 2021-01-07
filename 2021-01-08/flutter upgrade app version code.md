### flutter upgrade app version code


[android - Flutter: upgrade the version code for play store - Stack Overflow](https://stackoverflow.com/questions/53570575/flutter-upgrade-the-version-code-for-play-store "android - Flutter: upgrade the version code for play store - Stack Overflow")


 

```
Figured this one out. Documentation is not straight forward

in your pubspec.yaml change the version like this

version: 1.0.2+2
where the stuff is VER_NAME+VER_CODE

---

version: 1.0.0+2

prev was version: 1.0.0+1
```
