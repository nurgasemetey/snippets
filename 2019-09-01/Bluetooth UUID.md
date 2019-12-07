### Bluetooth UUID


[Android: How do bluetooth UUIDs work? - Stack Overflow](https://stackoverflow.com/questions/13964342/android-how-do-bluetooth-uuids-work)




```shell
The UUID is used for uniquely identifying information. It identifies a particular service provided by a Bluetooth device. The standard defines a basic BASE_UUID: 00000000-0000-1000-8000-00805F9B34FB.

Devices such as healthcare sensors can provide a service, substituting the first eight digits with a predefined code. For example, a device that offers an RFCOMM connection uses the short code: 0x0003

So, an Android phone can connect to a device and then use the Service Discovery Protocol (SDP) to find out what services it provides (UUID).

In many cases, you don't need to use these fixed UUIDs. In the case your are creating a chat application, for example, one Android phone interacts with another Android phone that uses the same application and hence the same UUID.

So, you can set an arbitrary UUID for your application using, for example, one of the many random UUID generators on the web (for example).


```
