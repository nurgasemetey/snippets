### zuul timeout config 


[java - Which Spring Cloud Zuul timeout property to use when using the default setup? - Stack Overflow](https://stackoverflow.com/questions/56358124/which-spring-cloud-zuul-timeout-property-to-use-when-using-the-default-setup "java - Which Spring Cloud Zuul timeout property to use when using the default setup? - Stack Overflow")



[spring-cloud-zuul timeout configuration does not work - Stack Overflow](https://stackoverflow.com/questions/49525707/spring-cloud-zuul-timeout-configuration-does-not-work "spring-cloud-zuul timeout configuration does not work - Stack Overflow")



[Timeout configurations do not work · Issue #2201 · spring-cloud/spring-cloud-netflix](https://github.com/spring-cloud/spring-cloud-netflix/issues/2201 "Timeout configurations do not work · Issue #2201 · spring-cloud/spring-cloud-netflix")


 

```bash
If you want to configure timeout in Zuul you have two options ,

If you have configured Zuul to use service discovery, you need to configure these timeouts with the below Ribbon properties

ribbon.ReadTimeout 
ribbon.SocketTimeout

If you have configured Zuul routes by specifying URLs then use below properties ,as per your configuration you need to use this one

zuul.host.connect-timeout-millis
zuul.host.socket-timeout-millis

---
Try to define the below properties instead if you are using Zuul withe Eureka.

ribbon:
  ReadTimeout: 60000
  ConnectTimeout: 20000
If you are using Zuul with Eureka, Zuul will use RibbonRoutingFilter for routing instead of SimpleHostRoutingFilter. In this case, HTTP requests are handled by Ribbon.


```
