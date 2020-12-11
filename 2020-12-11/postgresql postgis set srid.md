### postgresql postgis set srid


[postgis - Why ST_SRID cause Geoserver generated SQL query to run about 500x slower? - Geographic Information Systems Stack Exchange](https://gis.stackexchange.com/questions/82368/why-st-srid-cause-geoserver-generated-sql-query-to-run-about-500x-slower "postgis - Why ST_SRID cause Geoserver generated SQL query to run about 500x slower? - Geographic Information Systems Stack Exchange")




```
ALTER TABLE mytable 
ALTER COLUMN geom TYPE Geometry(Point,4326) 
USING ST_SetSRID(geom,4326);

```
