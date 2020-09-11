###  spring data jpa ignore field database


[java - What is the easiest way to ignore a JPA field during persistence? - Stack Overflow](https://stackoverflow.com/questions/1281952/what-is-the-easiest-way-to-ignore-a-jpa-field-during-persistence#:~:text=To%20ignore%20a%20field%2C%20annotate,field%20when%20converting%20to%20JSON.&text=25-,To%20ignore%20a%20field%2C%20annotate%20it%20with%20%40Transient%20so%20it,not%20be%20mapped%20by%20hibernate. "java - What is the easiest way to ignore a JPA field during persistence? - Stack Overflow")


 

```
@Transient - the JPA annotation marking a field as not persistable


```
