###  moment get all days of current week


[angularjs - How to get the Days b/w current week in moment.js - Stack Overflow](https://stackoverflow.com/questions/34871998/how-to-get-the-days-b-w-current-week-in-moment-js "angularjs - How to get the Days b/w current week in moment.js - Stack Overflow")


 

```
const getCurrentWeekDays = () => {
  const weekStart = moment().startOf('week');

  const days = [];
  for (let i = 0; i <= 6; i++) {
    days.push(moment(weekStart).add(i, 'days'));
  }

  return days;
}
```
