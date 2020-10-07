### javascript check contains letter


[Check if string contains any letter (Javascript/jquery) - Stack Overflow](https://stackoverflow.com/questions/61550004/check-if-string-contains-any-letter-javascript-jquery "Check if string contains any letter (Javascript/jquery) - Stack Overflow")




```
var regExp = /[a-zA-Z]/g;
var testString = "john";
            
if(regExp.test(testString)){
  /* do something if letters are found in your string */
} else {
  /* do something if letters are not found in your string */
}
```
