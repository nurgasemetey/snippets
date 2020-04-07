### field filter in list


[bohnman/squiggly: The Squiggly Filter is a Jackson JSON PropertyFilter, which selects properties of an object/list/map using a subset of the Facebook Graph API filtering syntax.](https://github.com/bohnman/squiggly "bohnman/squiggly: The Squiggly Filter is a Jackson JSON PropertyFilter, which selects properties of an object/list/map using a subset of the Facebook Graph API filtering syntax.")


 

```java
List<User> users = Arrays.asList(
        new User("Peter", 12, "Dinklage"), 
        new User("Lena", 13, "Heady"));
String filter = "firstName,age";
ObjectMapper objectMapper = Squiggly.init(new ObjectMapper(), filter);  
List<User> filteredUsers = SquigglyUtils.listify(objectMapper, users, User.class);

```
