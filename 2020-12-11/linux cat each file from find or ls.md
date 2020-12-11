### linux cat each file from find or ls







```
find -name "application.yml" -type f | xargs cat | grep port
```
