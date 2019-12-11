### Checking if dictionary is empty in python


[Python: Checking if a 'Dictionary' is empty doesn't seem to work - Stack Overflow](https://stackoverflow.com/questions/23177439/python-checking-if-a-dictionary-is-empty-doesnt-seem-to-work "Python: Checking if a 'Dictionary' is empty doesn't seem to work - Stack Overflow")




```python
test_dict = {}

if not test_dict:
    print "Dict is Empty"


if not bool(test_dict):
    print "Dict is Empty"


if len(test_dict) == 0:
    print "Dict is Empty"
```
