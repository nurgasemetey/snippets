###  moment get week day name from date


[javascript - Moment.js get day name from date - Stack Overflow](https://stackoverflow.com/questions/27669019/moment-js-get-day-name-from-date "javascript - Moment.js get day name from date - Stack Overflow")


 

```javascript
var mydate = "2017-06-28T00:00:00";
var weekDayName =  moment(mydate).format('dddd');
console.log(weekDayName);
```
