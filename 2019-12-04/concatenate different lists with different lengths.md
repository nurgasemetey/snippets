### concatenate different lists with different lengths


[python - Different column length PrettyTable - Stack Overflow](https://stackoverflow.com/questions/40377420/different-column-length-prettytable "python - Different column length PrettyTable - Stack Overflow")


 

```python
titles = ('Test1','Test2')
ListA = ("111", "222")
ListB = ("333",)
itertools.zip_longest(ListA,ListB,fillvalue="")
```
