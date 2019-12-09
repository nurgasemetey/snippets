### Convert Java Object to / from JSON


[Jackson 2 – Convert Java Object to / from JSON – Mkyong.com](https://www.mkyong.com/java/jackson-2-convert-java-object-to-from-json/ "Jackson 2 – Convert Java Object to / from JSON – Mkyong.com")




```java

        Staff staff = createStaff();

        try {

            // Java objects to JSON file
            mapper.writeValue(new File("c:\\test\\staff.json"), staff);

            // Java objects to JSON string - compact-print
            String jsonString = mapper.writeValueAsString(staff);

```
