###  onetomany and manytoone infinite loop, serialization


[Infinite loop with spring-boot in a one to many relation - Stack Overflow](https://stackoverflow.com/questions/30892298/infinite-loop-with-spring-boot-in-a-one-to-many-relation "Infinite loop with spring-boot in a one to many relation - Stack Overflow")


 

```java
Solution:

Use

@JsonManagedReference annotation for the first objects instantiated

@JsonBackReference annotation for the second objects instantiated

First:

@JsonManagedReference
@OneToMany(cascade = CascadeType.ALL, fetch = FetchType.LAZY, mappedBy = "lodger")
    private List<Reference> referenceList;
Second:

@JsonBackReference
@ManyToOne
    @JoinColumn(name = "lodgerId")
    private Lodger lodger;

```
