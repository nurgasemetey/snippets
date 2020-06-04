###  dictionary python iterate


[How to iterate through a dictionary in Python?](https://www.tutorialspoint.com/How-to-iterate-through-a-dictionary-in-Python#:~:text=There%20are%20two%20ways%20of,key%20in%20keys()%20list.&text=There%20is%20also%20items(),tuple%20having%20key%20and%20value. "How to iterate through a dictionary in Python?")


 

```python
>>> D1={1:'a', 2:'b', 3:'c'} 
>>> for k, v in D1.items():
   print (k, v)
1 a
2 b
3 cq


>>> D1 = {1:'a', 2:'b', 3:'c'} 
>>> for k in D1.keys():
   print (k, D1[k])
1 a
2 b
3 c
```
