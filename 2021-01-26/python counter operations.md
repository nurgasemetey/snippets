### python counter operations


[Counter - Python Module of the Week](https://pymotw.com/2/collections/counter.html "Counter - Python Module of the Week")



[8.3. collections — High-performance container datatypes — Python 2.7.18 documentation](https://docs.python.org/2.7/library/collections.html "8.3. collections — High-performance container datatypes — Python 2.7.18 documentation")



[How to add or increment single item of the Python Counter class - Stack Overflow](https://stackoverflow.com/questions/30001856/how-to-add-or-increment-single-item-of-the-python-counter-class "How to add or increment single item of the Python Counter class - Stack Overflow")


 

```
>>> c['d'] = 8
>>> c
Counter({'a': 23, 'd': 8, 'b': -9})

---

import collections

print collections.Counter(['a', 'b', 'c', 'a', 'b', 'b'])
print collections.Counter({'a':2, 'b':3, 'c':1})
print collections.Counter(a=2, b=3, c=1)


---
print '\nSubtraction:'
print c1 - c2

```
