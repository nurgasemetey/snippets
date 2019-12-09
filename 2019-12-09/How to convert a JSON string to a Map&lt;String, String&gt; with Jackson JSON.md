### How to convert a JSON string to a Map&lt;String, String&gt; with Jackson JSON


[java - How to convert a JSON string to a Map&lt;String, String&gt; with Jackson JSON - Stack Overflow](https://stackoverflow.com/questions/2525042/how-to-convert-a-json-string-to-a-mapstring-string-with-jackson-json?answertab=oldest#tab-top "java - How to convert a JSON string to a Map&lt;String, String&gt; with Jackson JSON - Stack Overflow")




```java
public void testJackson() throws IOException {  
    ObjectMapper mapper = new ObjectMapper(); 
    File from = new File("albumnList.txt"); 
    TypeReference<HashMap<String,Object>> typeRef 
            = new TypeReference<HashMap<String,Object>>() {};

    HashMap<String,Object> o = mapper.readValue(from, typeRef); 
    System.out.println("Got " + o); 
}   
```
