###  spring boot file upload multiple multipart


[How can I accept multiple multipart files in my Spring MVC REST controller - Stack Overflow](https://stackoverflow.com/questions/50560799/how-can-i-accept-multiple-multipart-files-in-my-spring-mvc-rest-controller "How can I accept multiple multipart files in my Spring MVC REST controller - Stack Overflow")


 

```java
    @PostMapping("/batch")
    @ApiOperation(value = "", nickname = "addAttachmentWithFiles")
    public List<Attachment> addBatch(@RequestParam("file") MultipartFile[] files,
                                     @RequestParam("moduleName") String moduleName,
                                     @RequestParam("entityId") String entityId,
                                     @RequestParam("orgId") String orgId
    )  {
```
