###  git search code


[How to grep (search) committed code in the Git history - Stack Overflow](https://stackoverflow.com/questions/2928584/how-to-grep-search-committed-code-in-the-git-history "How to grep (search) committed code in the Git history - Stack Overflow")


 

```
git rev-list --all | xargs git grep "cassandra"
```
