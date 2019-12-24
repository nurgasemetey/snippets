### No bluetooth controller


[Bluetooth Issue: &quot;No default controller available&quot; / Kernel &amp; Hardware / Arch Linux Forums](https://bbs.archlinux.org/viewtopic.php?id=213841)




```shell
rfkill block bluetooh 
rfkill unblock bluetooth
sudo systemctl restart bluetooth
```

