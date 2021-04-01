### python geopandas set crs


[geopandas - setting right projection crs to geodataframe to calculate in meters - Stack Overflow](https://stackoverflow.com/questions/57378829/setting-right-projection-crs-to-geodataframe-to-calculate-in-meters "geopandas - setting right projection crs to geodataframe to calculate in meters - Stack Overflow")


 

```
gdf = gpd.GeoDataFrame(df, geometry=gpd.points_from_xy(df['latitude'], df['longitude']),
                                     crs={'init' :'epsg:4326'})
gdf = gdf.to_crs(epsg=3763)
gdf['radius'] = gdf.geometry.buffer(50)
```
