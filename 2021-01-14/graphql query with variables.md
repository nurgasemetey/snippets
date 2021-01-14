### graphql query with variables


[graphql - Apollo Query with Variable - Stack Overflow](https://stackoverflow.com/questions/51522902/apollo-query-with-variable "graphql - Apollo Query with Variable - Stack Overflow")


 

```
let result = await client
          .query({
            query: firstQuery,
            variables: {
              "page_index": 100
            }
          });
```
