### pandas check object is nan


[Efficiently checking if arbitrary object is NaN in Python / numpy / pandas? - Stack Overflow](https://stackoverflow.com/questions/18689512/efficiently-checking-if-arbitrary-object-is-nan-in-python-numpy-pandas "Efficiently checking if arbitrary object is NaN in Python / numpy / pandas? - Stack Overflow")


 

```
if val.dtype == float and np.isnan(val):
type(val) == float and np.isnan(val) 
```
