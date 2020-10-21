### mongodb find except


[pymongo - Mongodb find all except from one or two criteria - Stack Overflow](https://stackoverflow.com/questions/18439612/mongodb-find-all-except-from-one-or-two-criteria "pymongo - Mongodb find all except from one or two criteria - Stack Overflow")




```
db.bios.find( { Country: { $nin: ["Country1", "Country2"] } } )
And $ne for just one country:

db.bios.find( { Country: { $ne: "Country1" } } )

```
