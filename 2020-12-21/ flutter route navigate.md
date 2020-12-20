###  flutter route navigate


[Flutter -- static route and dynamic route](https://programming.vip/docs/flutter-static-route-and-dynamic-route.html "Flutter -- static route and dynamic route")


 

```
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Static routing',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      routes: {
        '/page1':(context)=>Page1(title: "Main page",),
        '/page2':(context)=>Page2(title: "Second page",),
        '/page3':(context)=>Page3(title: "Third page",),
        '/page4':(context)=>Page4(title: "Fourth page",),
      },
      onUnknownRoute: (RouteSettings setting){
        String name=setting.name;
        print("No match to route");
        return new MaterialPageRoute(builder: (context){
          return new ErrorPage(title: "No matching pages",);
        });
      },
      home: Page1(title: "Main page",),
    );
  }
}

Navigator.pushNamed(context, "/page2");

```
