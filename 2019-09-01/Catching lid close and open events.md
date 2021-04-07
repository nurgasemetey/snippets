### Catching lid close and open events



[14.04 - Catch lid close and open events - Ask Ubuntu](https://askubuntu.com/questions/525995/catch-lid-close-and-open-events)




```shell
The script you want to call when the lid opens or closes has to be stored
in /etc/acpi/lid.sh.

Then there has to be created the correct file /etc/acpi/events/lm_lid with the content as follows:

event=button/lid.*
action=/etc/acpi/lid.sh
Reboot your system to let this take effect. Or maybe it is enough to restart your ACPI using

sudo /etc/init.d/acpid restart
```
