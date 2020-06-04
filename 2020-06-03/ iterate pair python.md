###  iterate pair python


[python - Iterate over all pairs of consecutive items in a list - Stack Overflow](https://stackoverflow.com/questions/21303224/iterate-over-all-pairs-of-consecutive-items-in-a-list "python - Iterate over all pairs of consecutive items in a list - Stack Overflow")


 

```python
>>> l = [1, 7, 3, 5]
>>> for first, second in zip(l, l[1:]):
...     print first, second
```
