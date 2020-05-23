###  Running multiple emulators error


[android - Emulator: emulator: ERROR: Running multiple emulators with the same AVD is an experimental feature - Stack Overflow](https://stackoverflow.com/questions/55328499/emulator-emulator-error-running-multiple-emulators-with-the-same-avd-is-an-ex "android - Emulator: emulator: ERROR: Running multiple emulators with the same AVD is an experimental feature - Stack Overflow")


 

```
Removing the .lock files did the trick for me. Find the avd and remove the lock files. In a Mac .android/avd/'NAMEOFAVD.avd directory . The files I removed were hardware-qemu.ini.lock and multiinstance.lock.
```
