###  request python example http get body


[Requests: HTTP for Humans™ — Requests 2.23.0 documentation](https://requests.readthedocs.io/en/master/ "Requests: HTTP for Humans™ — Requests 2.23.0 documentation")


 

```python
>>> r = requests.get('https://api.github.com/user', auth=('user', 'pass'))
>>> r.status_code
200
>>> r.headers['content-type']
'application/json; charset=utf8'
>>> r.encoding
'utf-8'
>>> r.text
'{"type":"User"...'
>>> r.json()
{'private_gists': 419, 'total_private_repos': 77, ...}
```
