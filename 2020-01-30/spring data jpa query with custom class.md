### spring data jpa query with custom class


[Spring Data JPA - Reference Documentation](https://docs.spring.io/spring-data/jpa/docs/2.1.11.RELEASE/reference/html/#jpa.query-methods.at-query "Spring Data JPA - Reference Documentation")


 

```java
    @Query("select internalControl.biddingDepartment as biddingDepartment, count(internalControl.biddingCost) as biddingCount, sum(internalControl.biddingCost) as biddingTotalCost\n" +
            "from InternalControl internalControl\n" +
            "group by internalControl.biddingDepartment")
    List<GoodPurchaseStatistics> getGoodsPurchaseStatistics();


public interface GoodPurchaseStatistics {
    String getBiddingDepartment();
    Long getBiddingCount();
    Float getBiddingTotalCost();

}
```
