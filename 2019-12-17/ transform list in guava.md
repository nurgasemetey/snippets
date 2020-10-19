###  transform list in guava


[Filtering and Transforming Collections in Guava | Baeldung](https://www.baeldung.com/guava-filter-and-transform-a-collection#transform-a-collection "Filtering and Transforming Collections in Guava | Baeldung")


 

```java
    Function<String, Integer> function = new Function<String, Integer>() {
        @Override
        public Integer apply(String input) {
            return input.length();
        }
    };
 
    List<String> names = Lists.newArrayList("John", "Jane", "Adam", "Tom");
    Iterable<Integer> result = Iterables.transform(names, function);
```
