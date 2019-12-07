###  How can I dynamically add features to a GeoJSON file


[How can I dynamically add features to a GeoJSON file? - Geographic Information Systems Stack Exchange](https://gis.stackexchange.com/questions/103782/how-can-i-dynamically-add-features-to-a-geojson-file "How can I dynamically add features to a GeoJSON file? - Geographic Information Systems Stack Exchange")


 

```python
import json

# Load existing data
with open('test.json') as f:
  data = json.load(f)

# Add data 
feature = {}
feature['type'] = 'Feature'
feature['geometry'] = {'type': 'Point',
                       'coordinates': [10, 10],
                       }
feature['properties'] =  {'prop0': 'value1'}
data['features'].append(feature)

# Write JSON file with new data
with open('test.json', 'w') as f:
  f.write(json.dumps(data))
```
