### null check in kotlin


[Best way to null check in Kotlin? - Stack Overflow](https://stackoverflow.com/questions/37231560/best-way-to-null-check-in-kotlin)




```kotlin
device?.let {
                val deviceNew:Device = device.copy(
                        status = streamDeviceStatusData.status,
                        statusUpdateDate = Date(streamDeviceStatusData.ts*1000)
                )
                deviceService.update(}
```
