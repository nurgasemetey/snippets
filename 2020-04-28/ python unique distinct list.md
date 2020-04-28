###  python unique distinct list


[How to get unique values from a python list of objects - Stack Overflow](https://stackoverflow.com/questions/26043482/how-to-get-unique-values-from-a-python-list-of-objects "How to get unique values from a python list of objects - Stack Overflow")


 

```python
cars = [...] # A list of Car objects.

models = {car.model for car in cars}
```
