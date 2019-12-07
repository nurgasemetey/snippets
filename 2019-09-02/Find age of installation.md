### Find age of installation


[command line - How can I tell what date Ubuntu was installed? - Ask Ubuntu](https://askubuntu.com/questions/1352/how-can-i-tell-what-date-ubuntu-was-installed)




```shell
ls -alct /|tail -1|awk '{print $6, $7, $8}'
```
