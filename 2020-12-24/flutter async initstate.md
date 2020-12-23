### flutter async initstate


[dart - Is there a way to load async data on InitState method? - Stack Overflow](https://stackoverflow.com/questions/51901002/is-there-a-way-to-load-async-data-on-initstate-method "dart - Is there a way to load async data on InitState method? - Stack Overflow")




```
@override
        void initState () {
          super.initState();
          WidgetsBinding.instance.addPostFrameCallback((_){
            _asyncMethod();
          });

        }
```
