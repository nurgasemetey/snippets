### add mysql extension to geoserver 


[docker-geoserver/setup.sh at master · kartoza/docker-geoserver](https://github.com/kartoza/docker-geoserver/blob/master/scripts/setup.sh "docker-geoserver/setup.sh at master · kartoza/docker-geoserver")



[geoserver-docker-alpine/Dockerfile at master · gtrubach/geoserver-docker-alpine](https://github.com/gtrubach/geoserver-docker-alpine/blob/master/Dockerfile "geoserver-docker-alpine/Dockerfile at master · gtrubach/geoserver-docker-alpine")




```shell
#Extensions

array=(geoserver-$GS_VERSION-vectortiles-plugin.zip geoserver-$GS_VERSION-css-plugin.zip \
geoserver-$GS_VERSION-csw-plugin.zip geoserver-$GS_VERSION-wps-plugin.zip geoserver-$GS_VERSION-printing-plugin.zip \
geoserver-$GS_VERSION-libjpeg-turbo-plugin.zip geoserver-$GS_VERSION-control-flow-plugin.zip \
geoserver-$GS_VERSION-pyramid-plugin.zip geoserver-$GS_VERSION-gdal-plugin.zip \
geoserver-$GS_VERSION-sldservice-plugin.zip  \
geoserver-$GS_VERSION-importer-plugin.zip geoserver-$GS_VERSION-charts-plugin.zip
geoserver-$GS_VERSION-mysql-plugin.zip
)
```

