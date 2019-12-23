###  project in aggregate


[mongodb - Project only some fields of array items in sub document - Stack Overflow](https://stackoverflow.com/questions/40794762/project-only-some-fields-of-array-items-in-sub-document)


 

```js
db.collection.aggregate([ 
    { "$project": { 
        "name": 1, 
        "models": { 
            "$map": { 
                "input": "$models", 
                "as": "m", 
                "in": { 
                    "type": "$$m.body.type", 
                    "minprice": "$$m.body.minprice" 
                } 
            } 
        }  
    }} 
])
```
