###  projection in native query, mapping names in spring data  jpa


[Spring Data JPA Projection support for native queries](https://medium.com/swlh/spring-data-jpa-projection-support-for-native-queries-a13cd88ec166 "Spring Data JPA Projection support for native queries")


 

```java
public interface CustomerDetailsDTO {

    Integer getCustomerId();

    @Value("#{target.firstName + ' ' + target.lastName}")
    String getCustomerName();

    String getCity();

    String getCountry();

    @Value("#{@mapperUtility.buildOrderDTO(target.orderNumber, target.totalAmount)}")
    OrderDTO getOrder();
}
```
