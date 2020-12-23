### flutter read load multiple images 


[dart - Flutter: How to get a list of names of all images in 'assets' directory? - Stack Overflow](https://stackoverflow.com/questions/56544200/flutter-how-to-get-a-list-of-names-of-all-images-in-assets-directory "dart - Flutter: How to get a list of names of all images in 'assets' directory? - Stack Overflow")



[dart - Is there a way to load async data on InitState method? - Stack Overflow](https://stackoverflow.com/questions/51901002/is-there-a-way-to-load-async-data-on-initstate-method "dart - Is there a way to load async data on InitState method? - Stack Overflow")


 

```
  @override
  void initState() {
    WidgetsBinding.instance.addPostFrameCallback((_){
      _initImages();
    });

  }


Future _initImages() async {
  // >> To get paths you need these 2 lines
  final manifestContent = await DefaultAssetBundle.of(context).loadString('AssetManifest.json');

  final Map<String, dynamic> manifestMap = json.decode(manifestContent);
  // >> To get paths you need these 2 lines

  final imagePaths = manifestMap.keys
      .where((String key) => key.contains('images/'))
      .where((String key) => key.contains('.svg'))
      .toList();

  setState(() {
    someImages = imagePaths;
  });
}
```
