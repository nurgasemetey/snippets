###  Adding custom functionality to spring data


[Add Custom Functionality to a Spring Data Repository - DZone Java](https://dzone.com/articles/add-custom-functionality-to-a-spring-data-reposito "Add Custom Functionality to a Spring Data Repository - DZone Java")


 

```
public interface EmployeeRepositoryCustom {
    List<Employee> getFirstNamesLike(String firstName);
}



@Repository
@Transactional(readOnly = true)
public class EmployeeRepositoryImpl implements EmployeeRepositoryCustom {
    @PersistenceContext
    EntityManager entityManager;
    @Override
    public List<Employee> getFirstNamesLike(String firstName) {
        Query query = entityManager.createNativeQuery("SELECT em.* FROM spring_data_jpa_example.employee as em " +
                "WHERE em.firstname LIKE ?", Employee.class);
        query.setParameter(1, firstName + "%");
        return query.getResultList();
    }
}




@Repository
public interface EmployeeRepository extends JpaRepository<Employee,Long>, EmployeeRepositoryCustom {
}
```
