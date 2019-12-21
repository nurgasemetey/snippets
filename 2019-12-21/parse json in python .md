### parse json in python 


[Why can't Python parse this JSON data? - Stack Overflow](https://stackoverflow.com/questions/2835559/why-cant-python-parse-this-json-data)


 

```python
import json
from pprint import pprint

with open('data.json') as f:
    data = json.load(f)

pprint(data)

```
