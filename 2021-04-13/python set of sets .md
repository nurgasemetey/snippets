### python set of sets 


[collections - How can I create a Set of Sets in Python? - Stack Overflow](https://stackoverflow.com/questions/5931291/how-can-i-create-a-set-of-sets-in-python "collections - How can I create a Set of Sets in Python? - Stack Overflow")


 

```
Python's complaining because the inner set objects are mutable and thus not hashable. The solution is to use frozenset for the inner sets, to indicate that you have no intention of modifying them.


```
