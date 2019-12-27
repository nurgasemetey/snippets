###  if not null else new


[android - Kotlin and idiomatic way to write, 'if not null, else...' based around mutable value - Stack Overflow](https://stackoverflow.com/questions/45877140/kotlin-and-idiomatic-way-to-write-if-not-null-else-based-around-mutable-v)


 

```koltin
device?.also {
                val deviceToUpdate = Device(device.id,
                        streamDeviceStatusData.id,
                    streamDeviceStatusData.name,
                    streamDeviceStatusData.type,
                    streamDeviceStatusData.status,
                    Date(streamDeviceStatusData.ts),
                    streamDeviceStatusData.orgId
                    )
                deviceService.update(deviceToUpdate)
            } ?: run {
                    val deviceNew = Device(
                            deviceId = streamDeviceStatusData.id,
                            name = streamDeviceStatusData.name,
                            type = streamDeviceStatusData.type,
                            status = streamDeviceStatusData.status,
                            statusUpdateDate = Date(streamDeviceStatusData.ts),
                            orgId = streamDeviceStatusData.orgId
                    )
                    deviceService.update(deviceNew)
            }
```
