###  Format datetime in pandas


[Python error : TypeError: Object of type 'Timestamp' is not JSON serializable' - Stack Overflow](https://stackoverflow.com/questions/50404559/python-error-typeerror-object-of-type-timestamp-is-not-json-serializable)


 

```python
row["timestamp_field_2"].strftime('%Y-%m-%d %H:%M:%S')
```
