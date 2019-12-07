### Can't create handler inside thread that has not called Looper.prepare


[android - Can't create handler inside thread that has not called Looper.prepare() - Stack Overflow](https://stackoverflow.com/questions/3875184/cant-create-handler-inside-thread-that-has-not-called-looper-prepare)


Can't create handler inside thread that has not called Looper.prepare

```java
activity.runOnUiThread(new Runnable() {
  public void run() {
    Toast.makeText(activity, "Hello", Toast.LENGTH_SHORT).show();
  }
});
```
