###  java list to map


[Java: How to convert List to Map - Stack Overflow](https://stackoverflow.com/questions/4138364/java-how-to-convert-list-to-map "Java: How to convert List to Map - Stack Overflow")



[How to Convert List to Map in Java | Baeldung](https://www.baeldung.com/java-list-to-map "How to Convert List to Map in Java | Baeldung")


 

```java
List<Hosting> list = new ArrayList<>();
list.add(new Hosting(1, "liquidweb.com", new Date()));
list.add(new Hosting(2, "linode.com", new Date()));
list.add(new Hosting(3, "digitalocean.com", new Date()));

//example 1
Map<Integer, String> result1 = list.stream().collect(
    Collectors.toMap(Hosting::getId, Hosting::getName));

System.out.println("Result 1 : " + result1);

//example 2
Map<Integer, String> result2 = list.stream().collect(
    Collectors.toMap(x -> x.getId(), x -> x.getName()));
```
