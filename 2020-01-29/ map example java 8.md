###  map example java 8


[Java 8 Streams map() examples – Mkyong.com](https://mkyong.com/java8/java-8-streams-map-examples/ "Java 8 Streams map() examples – Mkyong.com")


 

```java
        return attachmentService.getByInternalControlId(internalControlId).stream().map(x -> {
            x.setAttachmentUrl("kgm/internal-control-app-v2/internal-controls/" + x.getInternalControl().getId() + "/attachments/" + x.getId());
            return x;
        }).collect(Collectors.toList());
```
