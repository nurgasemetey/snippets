###  Parse csv in bash


[linux - How to parse a CSV file in Bash? - Stack Overflow](https://stackoverflow.com/questions/4286469/how-to-parse-a-csv-file-in-bash)


 

```shell
while IFS=, read -r col1 col2
do
    echo "I got:$col1|$col2"
done < myfile.csv
```
