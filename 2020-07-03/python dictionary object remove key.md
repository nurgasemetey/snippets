### python dictionary object remove key


[How to remove a key from a Python dictionary? - Stack Overflow](https://stackoverflow.com/questions/11277432/how-to-remove-a-key-from-a-python-dictionary "How to remove a key from a Python dictionary? - Stack Overflow")


 

```python
To delete a key regardless of whether it is in the dictionary, use the two-argument form of dict.pop():

my_dict.pop('key', None)
This will return my_dict[key] if key exists in the dictionary, and None otherwise. If the second parameter is not specified (ie. my_dict.pop('key')) and key does not exist, a KeyError is raised.

To delete a key that is guaranteed to exist, you can also use

del my_dict['key']
This will raise a KeyError if the key is not in the dictionary.



```
