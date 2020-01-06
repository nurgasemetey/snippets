### Extract only file in zip using unzip


[zip - Extract only a specific file from a zipped archive to a given directory - Unix &amp; Linux Stack Exchange](https://unix.stackexchange.com/questions/14120/extract-only-a-specific-file-from-a-zipped-archive-to-a-given-directory "zip - Extract only a specific file from a zipped archive to a given directory - Unix &amp; Linux Stack Exchange")




```shell
unzip -p "$file" "DynamicSegmentsData.csv" > "$temp_file";
```
