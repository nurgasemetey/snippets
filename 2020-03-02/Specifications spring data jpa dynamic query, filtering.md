### Specifications spring data jpa dynamic query, filtering


[Spring Data JPA - Using Specifications to execute JPA Criteria Queries](https://www.logicbig.com/tutorials/spring-framework/spring-data/specifications.html "Spring Data JPA - Using Specifications to execute JPA Criteria Queries")



[Writing dynamic queries with Spring Data JPA | Dimitri's tutorials](https://dimitr.im/writing-dynamic-queries-with-spring-data-jpa "Writing dynamic queries with Spring Data JPA | Dimitri's tutorials")



[Spring Data JPA - Combining multiple Specifications](https://www.logicbig.com/tutorials/spring-framework/spring-data/combined-specifications.html "Spring Data JPA - Combining multiple Specifications")




 

```java
public class InvestmentSpecifications {

    public static Specification<Investment> getByStartYear(List<Integer> startYearList) {
        return (Specification<Investment>) (root, criteriaQuery, criteriaBuilder) -> root.get("startYear").in(startYearList);
    }
}

//Service
        Specification<Investment> specification = Specification
                .where((investmentFilter.getStartYearList() == null) ? null : InvestmentSpecifications.getByStartYear(investmentFilter.getStartYearList()));
        return investmentRepository.findAll(specification);
```
