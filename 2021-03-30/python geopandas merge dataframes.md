### python geopandas merge dataframes


[Merging Data — GeoPandas 0.9.0 documentation](https://geopandas.org/docs/user_guide/mergingdata.html "Merging Data — GeoPandas 0.9.0 documentation")


 

```
# One GeoDataFrame of countries, one of Cities.
# Want to merge so we can get each city's country.
In [15]: countries.head()
Out[15]: 
                                            geometry                   country
0  MULTIPOLYGON (((180.000000000 -16.067132664, 1...                      Fiji
1  POLYGON ((33.903711197 -0.950000000, 34.072620...                  Tanzania
2  POLYGON ((-8.665589565 27.656425890, -8.665124...                 W. Sahara
3  MULTIPOLYGON (((-122.840000000 49.000000000, -...                    Canada
4  MULTIPOLYGON (((-122.840000000 49.000000000, -...  United States of America

In [16]: cities.head()
Out[16]: 
           name                           geometry
0  Vatican City  POINT (12.453386545 41.903282180)
1    San Marino  POINT (12.441770158 43.936095835)
2         Vaduz   POINT (9.516669473 47.133723774)
3    Luxembourg   POINT (6.130002806 49.611660379)
4       Palikir  POINT (158.149974324 6.916643696)

# Execute spatial join
In [17]: cities_with_country = geopandas.sjoin(cities, countries, how="inner", op='intersects')

In [18]: cities_with_country.head()
Out[18]: 
             name                           geometry  index_right  country
0    Vatican City  POINT (12.453386545 41.903282180)          141    Italy
1      San Marino  POINT (12.441770158 43.936095835)          141    Italy
192          Rome  POINT (12.481312563 41.897901485)          141    Italy
2           Vaduz   POINT (9.516669473 47.133723774)          114  Austria
184        Vienna  POINT (16.364693097 48.201961137)          114  Austria
```
