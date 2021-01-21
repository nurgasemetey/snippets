###  python sort tuples by field


[python - How to sort a list/tuple of lists/tuples by the element at a given index? - Stack Overflow](https://stackoverflow.com/questions/3121979/how-to-sort-a-list-tuple-of-lists-tuples-by-the-element-at-a-given-index "python - How to sort a list/tuple of lists/tuples by the element at a given index? - Stack Overflow")


 

```
sorted(data, key=lambda tup: (tup[1],tup[2]) )
```
