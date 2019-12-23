### mongoexport with query and isodate


[mongodb - MondoDB: mongoexport with a --query for ISODate - Stack Overflow](https://stackoverflow.com/questions/41809568/mondodb-mongoexport-with-a-query-for-isodate)




```shell
mongoexport --db event --collection event --query "{'date':{'$gte':ISODate('2017-03-01T23:00:00Z')}}" --type=csv --fields _id,attendees,date --out "c:\myfile.csv"?
```
