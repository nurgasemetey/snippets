### the JSON object must be str, not 'bytes


[TypeError: the JSON object must be str, not 'bytes' - Python - fixer.io - Stack Overflow](https://stackoverflow.com/questions/51862380/typeerror-the-json-object-must-be-str-not-bytes-python-fixer-io "TypeError: the JSON object must be str, not 'bytes' - Python - fixer.io - Stack Overflow")




```python
rdata = json.loads(data.decode(), parse_float=float)

```
