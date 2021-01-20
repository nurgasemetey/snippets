### python list of values dictionary


[python - How can I get list of values from dict? - Stack Overflow](https://stackoverflow.com/questions/16228248/how-can-i-get-list-of-values-from-dict "python - How can I get list of values from dict? - Stack Overflow")


 

```
Yes it's the exact same thing in Python 2:

d.values()

In Python 3 (where dict.values returns a view of the dictionary’s values instead):

list(d.values())
```
