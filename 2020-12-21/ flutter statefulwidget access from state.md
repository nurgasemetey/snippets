###  flutter statefulwidget access from state


[dart - Passing data to StatefulWidget and accessing it in it's state in Flutter - Stack Overflow](https://stackoverflow.com/questions/50287995/passing-data-to-statefulwidget-and-accessing-it-in-its-state-in-flutter "dart - Passing data to StatefulWidget and accessing it in it's state in Flutter - Stack Overflow")


 

```
class RecordPage extends StatefulWidget {
  final Record recordObject;

  RecordPage({Key key, @required this.recordObject}) : super(key: key);

  @override
  _RecordPageState createState() => new _RecordPageState(recordObject);
}

class _RecordPageState extends State<RecordPage> {
  Record  recordObject
 _RecordPageState(this. recordObject);  //constructor
  @override
  Widget build(BuildContext context) {.    //closure has access
   //.....
  }
}
```
