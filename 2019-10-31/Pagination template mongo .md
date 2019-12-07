### Pagination template mongo 


[Spring-Mongo Template Pagination - Muhammad Ahsan - Medium](https://medium.com/@AADota/spring-mongo-template-pagination-92fa93c50d5c "Spring-Mongo Template Pagination - Muhammad Ahsan - Medium")


 

```java
Pageable pageable = PageRequest.of(0, 10);

Query patientsDynamicQuery = new Query().with(pageable);
// Add criteria's according to your wish to patientsDynamicQuery
List<Patient> filteredPatients = 
mongoTemplate.find(patientsDynamicQuery, Patient.class, "patient");
Page<Patient> patientPage = PageableExecutionUtils.getPage(
        filteredPatients,
        pageable,
        () -> mongoTemplate.count(patientsDynamicQuery, Patient.class));
```
