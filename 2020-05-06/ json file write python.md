###  json file write python


[python - How do I write JSON data to a file? - Stack Overflow](https://stackoverflow.com/questions/12309269/how-do-i-write-json-data-to-a-file "python - How do I write JSON data to a file? - Stack Overflow")


 

```python
import json

data = {}
data['people'] = []
data['people'].append({
    'name': 'Scott',
    'website': 'stackabuse.com',
    'from': 'Nebraska'
})
data['people'].append({
    'name': 'Larry',
    'website': 'google.com',
    'from': 'Michigan'
})
data['people'].append({
    'name': 'Tim',
    'website': 'apple.com',
    'from': 'Alabama'
})

with open('data.txt', 'w') as outfile:
    json.dump(data, outfile)
```
