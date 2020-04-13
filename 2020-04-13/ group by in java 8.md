###  group by in java 8


[Guide to Java 8 groupingBy Collector | Baeldung](https://www.baeldung.com/java-groupingby-collector "Guide to Java 8 groupingBy Collector | Baeldung")


 

```java
Map<BlogPostType, List<BlogPost>> postsPerType = posts.stream()
  .collect(groupingBy(BlogPost::getType));
```
