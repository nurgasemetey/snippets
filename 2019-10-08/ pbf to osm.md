###  pbf to osm


[PostGIS OSM Import | GIS-Blog.com](https://www.gis-blog.com/postgis-osm-import/)


 

```shell
CREATE EXTENSION postgis;
CREATE EXTENSION hstore;
osm2pgsql -d osm_public_transportation -H 192.168.1.121 -U postgres  --hstore -S default.style --slim ulid443_station2_01.pbf
```
