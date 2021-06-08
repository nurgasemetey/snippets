### pandas subset column keyerror ignore


[Ignore warning Pandas KeyError: value not in index - Stack Overflow](https://stackoverflow.com/questions/56707889/ignore-warning-pandas-keyerror-value-not-in-index "Ignore warning Pandas KeyError: value not in index - Stack Overflow")


 

```
l = ['A', 'B', 'C', 'D']
df[df.columns.intersection(l)]

```
