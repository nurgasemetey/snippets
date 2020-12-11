### linux rename user







```
id oldname
usermod -l newname oldname
groupmod -n newname oldname
usermod -d /home/newname -m newname
usermod -c “New_real_name” newname
id newname

```
