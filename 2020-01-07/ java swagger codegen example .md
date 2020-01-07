###  java swagger codegen example 


[scala - Possible to change the package name when generating client code - Stack Overflow](https://stackoverflow.com/questions/37050768/possible-to-change-the-package-name-when-generating-client-code "scala - Possible to change the package name when generating client code - Stack Overflow")



[\[BUG\]missing swagger input or config · Issue #6442 · swagger-api/swagger-codegen](https://github.com/swagger-api/swagger-codegen/issues/6442 "[BUG]missing swagger input or config · Issue #6442 · swagger-api/swagger-codegen")



[Swagger 3.0.0 codegen failed java.lang.RuntimeException: missing swagger input or config - Stack Overflow](https://stackoverflow.com/questions/47301891/swagger-3-0-0-codegen-failed-java-lang-runtimeexception-missing-swagger-input-o "Swagger 3.0.0 codegen failed java.lang.RuntimeException: missing swagger input or config - Stack Overflow")


 use swagger 3.0.0

```shell
config file
{
    "modelPackage" : "com.parabol.licensemanager",
    "apiPackage" : "com.parabol.licensemanager",
    "groupId": "com.parabol.licensemanager",
    "artifactId": "java-sdk"
}



java -jar modules/swagger-codegen-cli/target/swagger-codegen-cli.jar generate -i /mnt/fd68f224-e30e-4ea0-8bd8-7f2a4c4d5ab0/nurgasemetey-environment/Spring/microservices-workspace/TKM/license-manager/sdk/openapi.json -l java -o /home/nurgasemetey/Desktop/tmp/licensemanagersdk -c /mnt/fd68f224-e30e-4ea0-8bd8-7f2a4c4d5ab0/nurgasemetey-environment/Spring/microservices-workspace/TKM/license-manager/sdk/java/config.json

```
