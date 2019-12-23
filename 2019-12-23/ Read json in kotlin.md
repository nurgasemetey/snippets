###  Read json in kotlin


[json - How to use jackson to deserialize to Kotlin collections - Stack Overflow](https://stackoverflow.com/questions/33368328/how-to-use-jackson-to-deserialize-to-kotlin-collections)


 

```kotlin
import com.fasterxml.jackson.module.kotlin.*  
val JSON = jacksonObjectMapper()  // keep around and re-use
val myList: List<String> = JSON.readValue("""["a","b","c"]""")
```
