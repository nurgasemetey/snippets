###  echo without new line


[linux - echo &quot;string&quot; | xclip -selection clipboard , copies the 'string' but also adds a new line to it. how to fix this? - Stack Overflow](https://stackoverflow.com/questions/16927974/echo-string-xclip-selection-clipboard-copies-the-string-but-also-adds-a "linux - echo &quot;string&quot; | xclip -selection clipboard , copies the 'string' but also adds a new line to it. how to fix this? - Stack Overflow")


 

```
echo -n "string" | xclip -selection clipboard

```
