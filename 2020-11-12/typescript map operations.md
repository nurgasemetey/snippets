### typescript map operations


[TypeScript Map Example- HowToDoInJava](https://howtodoinjava.com/typescript/maps/ "TypeScript Map Example- HowToDoInJava")




```
let nameAgeMapping = new Map();
 
//Set entries
nameAgeMapping.set("Lokesh", 37);
nameAgeMapping.set("Raj", 35);
nameAgeMapping.set("John", 40);
 
//Get entries
nameAgeMapping.get("John");     //40
 
//Check entry is present or not
nameAgeMapping.has("Lokesh");       //true
nameAgeMapping.has("Brian");        //false
 
//Size of Map with 
nameAgeMapping.size;                //3
 
//Delete an entry
nameAgeMapping.delete("Lokesh");    // true
 
//Clear whole Map
nameAgeMapping.clear();             //Clear all entries
```
