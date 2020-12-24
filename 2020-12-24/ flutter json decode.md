###  flutter json decode


[How to decode JSON in Flutter? - Stack Overflow](https://stackoverflow.com/questions/51601519/how-to-decode-json-in-flutter "How to decode JSON in Flutter? - Stack Overflow")


 

```
import 'dart:convert';


jsonDecode()


json.decode()


final manifestContent = await DefaultAssetBundle.of(context).loadString('AssetManifest.json');
    // print(manifestContent);
    final Map<String, dynamic> manifestMap = json.decode(manifestContent);
```
