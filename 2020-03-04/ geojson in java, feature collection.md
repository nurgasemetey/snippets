###  geojson in java, feature collection


[opendatalab-de/geojson-jackson: GeoJson POJOs for Jackson - serialize and deserialize objects with ease](https://github.com/opendatalab-de/geojson-jackson "opendatalab-de/geojson-jackson: GeoJson POJOs for Jackson - serialize and deserialize objects with ease")


 

```java
FeatureCollection featureCollection = 
	new ObjectMapper().readValue(inputStream, FeatureCollection.class);

```
