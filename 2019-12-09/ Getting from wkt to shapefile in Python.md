###  Getting from wkt to shapefile in Python


[Getting from wkt to shapefile in Python? - Geographic Information Systems Stack Exchange](https://gis.stackexchange.com/questions/120146/getting-from-wkt-to-shapefile-in-python "Getting from wkt to shapefile in Python? - Geographic Information Systems Stack Exchange")


 

```python
#Since you've already got a list of dicts, you can use Shapely (to manage the geometry) and Fiona (to write the shape #file).
from shapely.geometry import mapping
from shapely.wkt import loadsc
from fiona import collection

schema = {'geometry': 'Point', 'properties': {'atribute1':'value', 'atribute2':'value'}}

with collection("output.shp", "w", "ESRI Shapefile", schema) as output:
    for point in points:
        geometry = loads(point['wkt'])
        output.write({'properties':{'atribute1': point['atribute1'],
                                    'atribute2': point['atribute2']},
                      'geometry': mapping(geometry)
```
