###  java 8 edit in stream


[Java 8 Streams peek() API | Baeldung](https://www.baeldung.com/java-streams-peek-api "Java 8 Streams peek() API | Baeldung")


 On top of that, peek() can be useful in another scenario: when we want to alter the inner state of an element. For example, let's say we want to convert all user's name to lowercase before printing them:



```
Stream<User> userStream = Stream.of(new User("Alice"), new User("Bob"), new User("Chuck"));
userStream.peek(u -> u.setName(u.getName().toLowerCase()))
  .forEach(System.out::println);


        List<Transaction> transactions = kbosClient.getTransactionsByProjectId(projectId);

        return transactions.stream().peek((x) -> {
            if(x.getInvestmentInThisYear().equals(new BigDecimal(0))) {
                x.setInvestmentInThisYear(x.getInvestmentSb());
            }
        }).collect(Collectors.toList());
```
