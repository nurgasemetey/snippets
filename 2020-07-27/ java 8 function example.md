###  java 8 function example


[Java 8 Function Examples - Mkyong.com](https://mkyong.com/java8/java-8-function-examples/ "Java 8 Function Examples - Mkyong.com")


 

```
        Function<String, Integer> func = x -> x.length();

        Integer apply = func.apply("mkyong");   // 6

        System.out.println(apply);

       Function<NewProject, String> func = x -> {
									if (x.getStatus() == null) return "";
									else return Constants.NEW_PROJECT_LOOKUP_MAP.get(x.getStatus());
								};
								setCustomFunction(func);

```
