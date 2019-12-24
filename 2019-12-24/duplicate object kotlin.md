### duplicate object kotlin


[How can I duplicate an object to another object, without changing the base object in Kotlin? - Stack Overflow](https://stackoverflow.com/questions/50237384/how-can-i-duplicate-an-object-to-another-object-without-changing-the-base-objec)




```kotlin
val deviceNew:Device = device.copy(
                        status = streamDeviceStatusData.status,
                        statusUpdateDate = Date(streamDeviceStatusData.ts*1000)
                )
```
