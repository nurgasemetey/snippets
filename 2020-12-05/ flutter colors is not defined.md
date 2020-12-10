###  flutter colors is not defined


[Flutter The named parameter 'colors' isn't defined in SweepGradient - Stack Overflow](https://stackoverflow.com/questions/63863187/flutter-the-named-parameter-colors-isnt-defined-in-sweepgradient "Flutter The named parameter 'colors' isn't defined in SweepGradient - Stack Overflow")


 

```
This happened to me as well after I upgraded to the latest stable flutter version 1.12. I fixed it doing following:

Type in terminal: flutter clean
Under File --> Invalidate Caches / Restart (click this option)
Afterwards everything worked like a charm again.
```
