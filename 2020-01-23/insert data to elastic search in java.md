### insert data to elastic search in java


[Guide to Elasticsearch in Java | Baeldung](https://www.baeldung.com/elasticsearch-java "Guide to Elasticsearch in Java | Baeldung")




```java
IndexResponse indexResponse = esTemplate.getClient().prepareIndex(indexName, typeName).setId(elasticId).setSource(internalControlElasticMap).get();
```
