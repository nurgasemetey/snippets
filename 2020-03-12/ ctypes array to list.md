###  ctypes array to list


[Python Ctypes: Convert returned C array to python list, WITHOUT numpy - Stack Overflow](https://stackoverflow.com/questions/26531611/python-ctypes-convert-returned-c-array-to-python-list-without-numpy "Python Ctypes: Convert returned C array to python list, WITHOUT numpy - Stack Overflow")


 

```python
getWeights_function_handler.restype = POINTER(double_c)

weights = getWeights_function_handler()
list = [weights[i] for i in xrange(ARRAY_SIZE_I_KNOW_IN_ADVANCE)]

```
