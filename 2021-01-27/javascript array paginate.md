### javascript array paginate


[Paginate Javascript array - Stack Overflow](https://stackoverflow.com/questions/42761068/paginate-javascript-array "Paginate Javascript array - Stack Overflow")


 

```
function paginate(array, page_size, page_number) {
  // human-readable page numbers usually start with 1, so we reduce 1 in the first argument
  return array.slice((page_number) * page_size, (page_number+1) * page_size);
}
```
