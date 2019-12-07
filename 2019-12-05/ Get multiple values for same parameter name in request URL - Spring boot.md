###  Get multiple values for same parameter name in request URL - Spring boot


[java - Get multiple values for same parameter name in request URL - Spring boot - Stack Overflow](https://stackoverflow.com/questions/52502778/get-multiple-values-for-same-parameter-name-in-request-url-spring-boot "java - Get multiple values for same parameter name in request URL - Spring boot - Stack Overflow")


 

```java
public void invoice(@RequestParam(name="invoiceNo") List<String> invoiceNos, @RequestParam(name="invoiceDate") List<String> invoiceDates) {

```
