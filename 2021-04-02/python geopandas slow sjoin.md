### python geopandas slow sjoin


[python - geopandas spatial join extremely slow - Geographic Information Systems Stack Exchange](https://gis.stackexchange.com/questions/175228/geopandas-spatial-join-extremely-slow "python - geopandas spatial join extremely slow - Geographic Information Systems Stack Exchange")


 

```
What's likely going on here is that only the dataframe on the right is fed into the rtree index: https://github.com/geopandas/geopandas/blob/master/geopandas/tools/sjoin.py#L48-L55 Which for an op="intersects" run would mean the Polygon was fed into the index, so for every point, the corresponding polygon is found through the rtree index.

But for op="within", the geodataframes are flipped since the operation is actually the inverse of contains: https://github.com/geopandas/geopandas/blob/master/geopandas/tools/sjoin.py#L41-L43

So what happened when you switched the op from op="intersects" to op="within" is that for every polygon, the corresponding points are found through the rtree index, which in your case sped up the query.


```
