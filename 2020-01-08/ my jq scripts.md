###  my jq scripts





 

```shell
##for osrm
jq ".matchings[] | .legs[]| .annotation | .nodes" 657-06-00-06-45-match.json
```

