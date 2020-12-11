### bash check if string empty





 Brackets with -z option tests for string emptiness

```
if [ -z "$1" ] || [ -z "$2" ]  || [ -z "$3" ] ; then   
	log "Some arguments are empty"
    exit 1 
fi
```
