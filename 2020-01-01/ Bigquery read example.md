###  Bigquery read example


[GCS temp location to store temp files · Issue #541 · GoogleCloudPlatform/DataflowJavaSDK](https://github.com/GoogleCloudPlatform/DataflowJavaSDK/issues/541 "GCS temp location to store temp files · Issue #541 · GoogleCloudPlatform/DataflowJavaSDK")


 

```java
        TemplateOptions options = PipelineOptionsFactory.create()
                .as(TemplateOptions.class);
        options.setProject("kgm-traffic-221812");
        options.setStagingLocation("gs://bucket");
        options.setTempLocation("gs://bucket");
```
