### Read lines and match against pattern 


[bash - Read lines and match against pattern - Unix &amp; Linux Stack Exchange](https://unix.stackexchange.com/questions/190814/read-lines-and-match-against-pattern)


 

```shell
#!/bin/bash
while read line; do
  if [[ $line =~ bird ]] ; then echo $line; fi
done <foo.text
```
