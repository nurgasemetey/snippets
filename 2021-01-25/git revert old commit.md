### git revert old commit


[Undo a Git merge that hasn't been pushed yet - Stack Overflow](https://stackoverflow.com/questions/2389361/undo-a-git-merge-that-hasnt-been-pushed-yet/27453620#27453620 "Undo a Git merge that hasn't been pushed yet - Stack Overflow")


 

```
You can use only two commands to revert a merge or restart by a specific commit:

git reset --hard commitHash (you should use the commit that you want to restart, eg. 44a587491e32eafa1638aca7738)
git push origin HEAD --force (Sending the new local master branch to origin/master)
Good luck and go ahead!
```
