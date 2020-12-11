### linux find and remove files with excluded directories







```
find . -name "target" -not \( -path "./speed_corridor/*" -o -path "./python-wkt/*" \) -type f -delete

```
