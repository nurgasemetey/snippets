### jpql integer to string spring boot


[jpa - Casting Integer to String in JPQL - Stack Overflow](https://stackoverflow.com/questions/46188918/casting-integer-to-string-in-jpql "jpa - Casting Integer to String in JPQL - Stack Overflow")


 

```
@Query("select CONCAT(internalControl.biddingDepartmentId,'') as biddingDepartment\n"
            + ",  count(internalControl.id) as biddingCount\n"
            + ",  sum(internalControl.biddingCost) as biddingCost\n"
            + ",  sum(internalControl.appropriateCost) as appropriateCost \n"
            + ", (select sum(internalControl.biddingCost) from InternalControl  internalControl) as biddingPercentage\n"
            + ",  avg(internalControl.discount) as discount\n" + "from InternalControl internalControl\n"
            + "where internalControl.fileNoYear = :year \n"
            + "group by internalControl.biddingDepartmentId\n" + "order by internalControl.biddingDepartmentId")
    List<GeneralStatistics> getGeneralStatisticsByRegion(@Param("year") Integer year);
```
