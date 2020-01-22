### static init in java 


[Working with static constructor in Java - Software Engineering Stack Exchange](https://softwareengineering.stackexchange.com/questions/228242/working-with-static-constructor-in-java "Working with static constructor in Java - Software Engineering Stack Exchange")


 

```java
public class Example{

    public final static Map<String, String> preFilledField;

    static{
        Map<String, String> tmp = new HashMap<>();
        //fill map
        preFilledField = Collections.unmodifiableMap(tmp);
    }
}
```
