###  Multipart file upload in spring


[Uploading Files with Spring MVC | Baeldung](https://www.baeldung.com/spring-file-upload "Uploading Files with Spring MVC | Baeldung")


 

```java
@PostMapping("/uploadFileWithAddtionalData")
public String submit(
  @RequestParam MultipartFile file, @RequestParam String name,
  @RequestParam String email, ModelMap modelMap) {
 
    modelMap.addAttribute("name", name);
    modelMap.addAttribute("email", email);
    modelMap.addAttribute("file", file);
    return "fileUploadView";
}
```
