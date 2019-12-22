###  docker container 139 nodejs


[node.js - docker container crashes with exited with code 139 - Stack Overflow](https://stackoverflow.com/questions/53124463/docker-container-crashes-with-exited-with-code-139?rq=1)


 

```shell
The issue may be caused by the fact that node:10-alpine is a tag where the underlying image may change with updates, so when you are building the same app without using compose it won't pull the most recent image, docker-compose will do a pull from the docker hub instead.

Images based on alpine may have some dependency issues that are quite hard to debug from one version to another, you can find some possibilities for this particular issue here

I was using the tag node:8-alpine in my application and I found out that the current latest node:8.15.1-alpine is causing the Exited with code 139 issue that was not present in the previous image node:8.15.0-alpine. Downgrading may be the easiest solution to solve this kind of issue, check if you are using bcrypt too.

Another option is to use a debian based image that will be less likely to have this kind of issues (just consider it's slighly bigger in size).


```
