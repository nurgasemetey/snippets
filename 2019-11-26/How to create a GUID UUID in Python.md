###  How to create a GUID/UUID in Python


[How to create a GUID/UUID in Python - Stack Overflow](https://stackoverflow.com/questions/534839/how-to-create-a-guid-uuid-in-python "How to create a GUID/UUID in Python - Stack Overflow")


 

```python
>>> import uuid
>>> uuid.uuid4()
UUID('bd65600d-8669-4903-8a14-af88203add38')
>>> str(uuid.uuid4())
'f50ec0b7-f960-400d-91f0-c42a6d44e3d0'
>>> uuid.uuid4().hex
'9fe2c4e93f654fdbb24c02b15259716c'
```
