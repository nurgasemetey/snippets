### bash uppercase


[linux - How to get Month in all upper case - Unix &amp; Linux Stack Exchange](https://unix.stackexchange.com/questions/377849/how-to-get-month-in-all-upper-case "linux - How to get Month in all upper case - Unix &amp; Linux Stack Exchange")




```
MONTH_NAME=$(date +%B | tr '[:lower:]' '[:upper:]')

```
