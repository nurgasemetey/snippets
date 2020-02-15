### handle exceptions in requests in python


[python - handling \[Errno 111\] Connection refused return by requests in flask - Stack Overflow](https://stackoverflow.com/questions/18353891/handling-errno-111-connection-refused-return-by-requests-in-flask "python - handling [Errno 111] Connection refused return by requests in flask - Stack Overflow")




```python
try:
    req = requests.post(buildApiUrl.getUrl('user') + "/login", data=payload)
except requests.exceptions.RequestException:
    # Handle exception ..
```
