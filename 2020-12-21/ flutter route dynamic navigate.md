###  flutter route dynamic navigate





 

```
Navigator.push(
    context,
    MaterialPageRoute(
        builder: (context)=>NewsDetail(s_new: news[index],),
    )
);


class NewsDetail extends StatelessWidget{
  final News s_new;

  NewsDetail({Key key,@required this.s_new}):super(key:key);
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text(this.s_new.title),),
      body: Center(
        child: Text(this.s_new.description),
      ),
    );
  }

}
```
