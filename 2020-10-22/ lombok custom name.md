###  lombok custom name


[json - Custom serialized and deserialized field names with lombok - Stack Overflow](https://stackoverflow.com/questions/49886553/custom-serialized-and-deserialized-field-names-with-lombok "json - Custom serialized and deserialized field names with lombok - Stack Overflow")


 

```
public class PrivacySettings {

    @Setter(onMethod_ = { @JsonSetter("CDO_Name__c") })
    @Getter(onMethod_ = { @JsonGetter("chiefDataOfficerName") })
    private String chiefDataOfficerName;
}
```
