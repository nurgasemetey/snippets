###  log4j arguments


[java - How to log the second argument in log4j - Stack Overflow](https://stackoverflow.com/questions/37755046/how-to-log-the-second-argument-in-log4j "java - How to log the second argument in log4j - Stack Overflow")


 

```
LogManager.getLogger(SomeName.class.getName()).info("Message: {}, Detail: {}", message, detail);

```
