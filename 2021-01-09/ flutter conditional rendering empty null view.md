###  flutter conditional rendering empty null view


[How to present an empty view in flutter? - Stack Overflow](https://stackoverflow.com/questions/53455358/how-to-present-an-empty-view-in-flutter#:~:text=The%20recommended%20widget%20to%20show%20nothing%20is%20to%20use%20SizedBox%20.&text=When%20a%20build%20function%20returns,return%20%22new%20Container()%22. "How to present an empty view in flutter? - Stack Overflow")

[Widget build(BuildContext context) { Widget child; if (condition) { child = ... } else { child = ... } return new Container(child: child); }](https://stackoverflow.com/questions/49713189/how-to-use-conditional-statement-within-child-attribute-of-a-flutter-widget-cen "dart - How to use conditional statement within child attribute of a Flutter Widget (Center Widget) - Stack Overflow")
 

```
  _buildButton(style)

....


Widget _buildButton (Style style) {
    if (!style.isBought) {
      return (
          FlatButton(
            color: Colors.blueAccent,
            onPressed: () async {
              print("test");
            },
            child: Text('Buy ${style.title}'),
          )
      );
    }
    return new Container();
  }
```
