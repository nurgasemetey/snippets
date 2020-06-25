### spring boot environmental variable default value 


[java - Does application.yml support environment variables? - Stack Overflow](https://stackoverflow.com/questions/23027315/does-application-yml-support-environment-variables "java - Does application.yml support environment variables? - Stack Overflow")


 

```yaml
logging:
  level:
    root: ${LOGGING_LEVEL_ROOT:info}

```
