### pass copy reference python


[python Dictionary Mutable Clarification - Stack Overflow](https://stackoverflow.com/questions/40956687/python-dictionary-mutable-clarification "python Dictionary Mutable Clarification - Stack Overflow")


 

```python
from copy import deepcopy
myDict = {'one': ['1', '2', '3']}
def dictionary(dict1):
    dict2 = deepcopy(dict1)
    dict2['one'][0] = 'one'
    print dict2
```
