###  gcp set root password


[Get root password for Google Cloud Engine VM - Stack Overflow](https://stackoverflow.com/questions/35016795/get-root-password-for-google-cloud-engine-vm "Get root password for Google Cloud Engine VM - Stack Overflow")


 

```
Figured it out. The VM's in cloud engine don't come with a root password setup by default so you'll first need to change the password using

sudo passwd

If you do everything correctly, it should do something like this:

user@server[~]# sudo passwd
Changing password for user root.
New password: 
Retype new password: 
passwd: all authentication tokens updated successfully.
```
