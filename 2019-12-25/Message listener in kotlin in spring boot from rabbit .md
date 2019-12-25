### Message listener in kotlin in spring boot from rabbit 


[spring boot - Taking only specific message from @RabbitListener - Stack Overflow](https://stackoverflow.com/questions/56679595/taking-only-specific-message-from-rabbitlistener)


 

```kotlin
    @RabbitListener(queues = arrayOf("device-management-status"))
    fun receive(message: Message) {
```
