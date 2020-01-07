### add external jar in resources and include in pom

[maven - Add external library .jar to Spring boot .jar internal /lib - Stack Overflow](https://stackoverflow.com/questions/30207842/add-external-library-jar-to-spring-boot-jar-internal-lib "maven - Add external library .jar to Spring boot .jar internal /lib - Stack Overflow")

[java - Maven: best way of linking custom external JAR to my project? - Stack Overflow](https://stackoverflow.com/questions/5692256/maven-best-way-of-linking-custom-external-jar-to-my-project/45120371 "java - Maven: best way of linking custom external JAR to my project? - Stack Overflow")


```
<plugin>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-maven-plugin</artifactId>
    <configuration>
        <includeSystemScope>true</includeSystemScope>
    </configuration>
</plugin>

<dependency>
<groupId>com.microsoft.sqlserver</groupId>
<artifactId>sqljdbc41</artifactId>
<version>4.1</version>
<scope>system</scope>
<systemPath>${basedir}/src/main/resources/lib/sqljdbc41.jar</systemPath>
```
