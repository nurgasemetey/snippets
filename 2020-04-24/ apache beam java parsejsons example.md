###  apache beam java parsejsons example


[Apache-Beam/JacksonTransformsTest.java at a8edbb81f340578966400d106297c1732ca3b7fd · xsm110/Apache-Beam](https://github.com/xsm110/Apache-Beam/blob/a8edbb81f340578966400d106297c1732ca3b7fd/sdks/java/extensions/jackson/src/test/java/org/apache/beam/sdk/extensions/jackson/JacksonTransformsTest.java "Apache-Beam/JacksonTransformsTest.java at a8edbb81f340578966400d106297c1732ca3b7fd · xsm110/Apache-Beam")


 

```java
ObjectMapper customMapper =
        new ObjectMapper().configure(DeserializationFeature.FAIL_ON_UNKNOWN_PROPERTIES, false);

    PCollection<MyPojo> output =
        pipeline
            .apply(Create.of(EXTRA_PROPERTIES_JSONS))
            .apply(ParseJsons.of(MyPojo.class)
                .withMapper(customMapper)).setCoder(SerializableCoder.of(MyPojo.class));
```
