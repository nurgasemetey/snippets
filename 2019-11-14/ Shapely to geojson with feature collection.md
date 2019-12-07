###  Shapely to geojson with feature collection


[alekzvik/shapely-geojson: Set of classes to work better with GeoJson spec with Shapely classes.](https://github.com/alekzvik/shapely-geojson "alekzvik/shapely-geojson: Set of classes to work better with GeoJson spec with Shapely classes.")




```python
>>> feature1 = Feature(Point(1, 2), {'index': 1})
>>> feature2 = Feature(Point(3, 4), {'index': 2})
>>> features = [feature1, feature2]
>>> feature_collection = FeatureCollection(features)
>>> for feature in feature_collection:
...     print(feature.properties['index'])
...
1
2
>>> print(dumps(feature_collection, indent=2))
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [
          1.0,
          2.0
        ]
      },
      "properties": {
        "index": 1
      }
    },
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [
          3.0,
          4.0
        ]
      },
      "properties": {
        "index": 2
      }
    }
  ]
}
```
