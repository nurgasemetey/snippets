### linux large files directory sub







```
du -a /home | sort -n -r | head -n 5
du -a | sort -n -r | head -n 5

# human readable
du -hs * | sort -rh | head -5
du -Sh | sort -rh | head -5
find -type f -exec du -Sh {} + | sort -rh | head -n 5

```
