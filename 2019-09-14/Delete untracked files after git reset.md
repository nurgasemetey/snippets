### Delete untracked files after git reset


[git reset --hard HEAD leaves untracked files behind - Stack Overflow](https://stackoverflow.com/questions/4327708/git-reset-hard-head-leaves-untracked-files-behind#comment4702861_4327708)


 

```shell
git clean -f -d
```
