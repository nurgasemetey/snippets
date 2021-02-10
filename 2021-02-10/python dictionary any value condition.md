### python dictionary any value condition


[python - Check if any value of a dictionary matches a condition - Stack Overflow](https://stackoverflow.com/questions/12376079/check-if-any-value-of-a-dictionary-matches-a-condition "python - Check if any value of a dictionary matches a condition - Stack Overflow")


 

```
>>> pairs = { 'word1':0, 'word2':0, 'word3':2000, 'word4':64, 'word5':0, 'wordn':8 }
>>> any(v > 0 for v in pairs.itervalues())
True
>>> any(v > 3000 for v in pairs.itervalues())
False
```
