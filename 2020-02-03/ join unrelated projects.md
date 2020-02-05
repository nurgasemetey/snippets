###  join unrelated projects


[java - Spring Data JPA - Join unrelated entities by defining projections - Stack Overflow](https://stackoverflow.com/questions/45343233/spring-data-jpa-join-unrelated-entities-by-defining-projections "java - Spring Data JPA - Join unrelated entities by defining projections - Stack Overflow")


 

```java
@Query("select ce as complaintEntry, a as attachment from ComplaintEntry ce left join Attachment a on ce.id = a.refId where ce.internalEntry = true")
    List<ComplaintEntryAndAtachment> findComplaintEntryAndAtachment();

public interface ComplaintEntryAndAtachment {

    ComplaintEntry getComplaintEntry();
    Attachment getAttachment();
}
```
