### Data class example in kotlin


[Kotlin data class optional variable - Stack Overflow](https://stackoverflow.com/questions/47134138/kotlin-data-class-optional-variable)


 

```kotlin
data class Device (
    @Id
    val id:String?,
    val name:String? = "",
    val type:String,
    val status:String? = "INACTIVE",
    var statusUpdateDate:Date? = Date(0),
    var orgId:String
)
```
