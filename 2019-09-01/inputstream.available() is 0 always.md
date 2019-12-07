### inputstream.available() is 0 always


[java - inputstream.available() is 0 always - Stack Overflow](https://stackoverflow.com/questions/5826198/inputstream-available-is-0-always)




```shell
.available() can not be used in inter-process communication (serial included), since it only checks if there is data available (in input buffers) in current process.

In serial communication, when you send a messaga and then immediately call available() you will mostly get 0 as serial port did not yet reply with any data.

The solution is to use blocking read() in a separate thread (with interrupt() to end it):
```
