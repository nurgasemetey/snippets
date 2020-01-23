### delete document in elastic search


[Guide to Elasticsearch in Java | Baeldung](https://www.baeldung.com/elasticsearch-java "Guide to Elasticsearch in Java | Baeldung")




```java
DeleteResponse deleteResponse = esTemplate.getClient().prepareDelete(indexName, typeName, elasticId).get();
```
