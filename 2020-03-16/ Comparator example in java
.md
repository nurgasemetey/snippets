###  Comparator example in java



[Java 8 - Comparator thenComparing() example - Group by sort example](https://howtodoinjava.com/sort/sort-on-multiple-fields/ "Java 8 - Comparator thenComparing() example - Group by sort example")


 

```java
Comparator<Employee> compareByName = Comparator
                                                .comparing(Employee::getFirstName)
                                                .thenComparing(Employee::getLastName);
```
