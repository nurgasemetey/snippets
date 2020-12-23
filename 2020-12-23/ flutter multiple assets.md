###  flutter multiple assets


[Multiple assets in Flutter project - Stack Overflow](https://stackoverflow.com/questions/49467565/multiple-assets-in-flutter-project "Multiple assets in Flutter project - Stack Overflow")


 

```
# ❌ Don't Import every files inside assets folder, its tiring ❌             
assets:
  - assets/audio/celebrate.mp3
  - assets/audio/splash.mp3
  - assets/lottie/paper_plane.json
  - assets/lottie/celebration.json
  - assets/images/png/stats.png
  - assets/images/alert.svg

# ❌ Import all assets at once,🚨 Not allowed ❌
assets:
  - assets/        

# ✅ Just import every folders inside assets ✅
assets:
  - assets/lottie/
  - assets/images/svg/
  - assets/images/png/
  - assets/audio/
```
