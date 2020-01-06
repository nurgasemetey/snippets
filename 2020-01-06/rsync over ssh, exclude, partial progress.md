### rsync over ssh, exclude, partial progress


[How to copy files with rsync over SSH - Tutorials For Kyup.com](https://kyup.com/tutorials/copy-files-rsync-ssh/ "How to copy files with rsync over SSH - Tutorials For Kyup.com")


 

```shell
nohup rsync -azvvP -e ssh  --exclude="*DataWest.csv.zip" /media/hdstorage/FCDNEW/2019/5 administrator@192.168.150.220:/home/administrator/FCD > ~/log.log 2>&1 &
```
