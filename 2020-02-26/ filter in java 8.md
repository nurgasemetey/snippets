###  filter in java 8


[How to use filter() method in Java 8 | Java Code Geeks - 2020](https://www.javacodegeeks.com/2018/07/filter-method-java-8.html "How to use filter() method in Java 8 | Java Code Geeks - 2020")


 

```java
List<Dish> menu = ....
List<Dish> vegitarianDishes = menu.stream()
                                    .filter(d -> d.getVegitarian())
                                    .collect(Collectors.toList());
```
