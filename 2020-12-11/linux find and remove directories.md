### linux find and remove directories







```
find . -name target -type d -print0| xargs -0 rm -r --
find . -name "target" -type d -exec rm -r "{}" \;

```
