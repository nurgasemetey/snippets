###  postman generate date


postman generate date


 [date - How do I format {{$timestamp}} as MM/DD/YYYY in Postman? - Stack Overflow](https://stackoverflow.com/questions/47355150/how-do-i-format-timestamp-as-mm-dd-yyyy-in-postman "date - How do I format {{$timestamp}} as MM/DD/YYYY in Postman? - Stack Overflow")

```
Use Pre-request script tab to write javascript to get and save the date into a variable:


const dateNow= new Date();
pm.environment.set('currentDate', dateNow.toISOString());

and then use it in the request body as follows:

"currentDate": "{{currentDate}}"

```
