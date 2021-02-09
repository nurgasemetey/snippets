### node specific persion project


[javascript - How do I specify a local version of Node for a project? - Stack Overflow](https://stackoverflow.com/questions/24869959/how-do-i-specify-a-local-version-of-node-for-a-project "javascript - How do I specify a local version of Node for a project? - Stack Overflow")


 

```
NVM + .nvmrc

If you are using NVM like this, which you likely should, then you can indicate the nodejs version required for given project in a git-tracked .nvmrc file:

echo v10.15.1 > .nvmrc
This does not take effect automatically on cd, which is sane: the user must then do a:

nvm use
and now that version of node will be used for the current shell.

You can list the versions of node that you have with:

nvm list
.nvmrc is documented at: https://github.com/creationix/nvm/tree/02997b0753f66c9790c6016ed022ed2072c22603#nvmrc

Tested with NVM 0.33.11.
```
