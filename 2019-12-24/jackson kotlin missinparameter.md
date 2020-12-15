###  jackson kotlin missinparameter


[MissingKotlinParameterException: due to missing (therefore NULL) value for creator parameter … which is a non-nullable type · Issue #87 · FasterXML/jackson-module-kotlin](https://github.com/FasterXML/jackson-module-kotlin/issues/87)


 

```kotlin
ObjectMapper().registerModule(KotlinModule(nullisSameAsDefault = true)

```
