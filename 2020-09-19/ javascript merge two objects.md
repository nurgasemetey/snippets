###  javascript merge two objects


[javascript - Merge two objects with ES6 - Stack Overflow](https://stackoverflow.com/questions/39121695/merge-two-objects-with-es6 "javascript - Merge two objects with ES6 - Stack Overflow")


 

```
const decisions: any[] = query.docs.map((value) => {
                return {id: value.id, ...value.data()}
            });
```
