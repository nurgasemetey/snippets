###  Composite key in spring data jpa


[The best way to map a Composite Primary Key with JPA and Hibernate - Vlad Mihalcea](https://vladmihalcea.com/the-best-way-to-map-a-composite-primary-key-with-jpa-and-hibernate/ "The best way to map a Composite Primary Key with JPA and Hibernate - Vlad Mihalcea")


 

```java
@Embeddable
@Data
@AllArgsConstructor
@NoArgsConstructor
public class PersonId implements Serializable {
    private Long companyId;
    private Long employeeNumber;
}


@Entity
@Data
@Table(name = "person", schema = "PUBLIC")
@JsonIgnoreProperties({"hibernateLazyInitializer", "handler"})
public class Person implements Serializable {


    private static final long serialVersionUID = 3339991914431829220L;
    @EmbeddedId
    private PersonId id;

    String name;

    @ManyToOne(fetch = FetchType.LAZY, optional = false)
//    @JoinColumn(name = "parent_id", nullable = true)
    @JoinColumns({
            @JoinColumn(
                    name = "parent_company_id"
                    ),
            @JoinColumn(
                    name = "parent_employee_number")
    })
    @OnDelete(action = OnDeleteAction.NO_ACTION)
    private Person parent;


//    @OneToMany(fetch = FetchType.LAZY,mappedBy = "parent")
//    private Set<Person> children;


}

```
