###  java remove duplicates from list


[Remove duplicates from a list of objects based on property in Java 8 - Stack Overflow](https://stackoverflow.com/questions/29670116/remove-duplicates-from-a-list-of-objects-based-on-property-in-java-8 "Remove duplicates from a list of objects based on property in Java 8 - Stack Overflow")


 

```
HashSet<Object> seen=new HashSet<>();
employee.removeIf(e->!seen.add(e.getID()));

---
//Remove duplicates from KBOS
HashSet<String> seen=new HashSet<>();
geometryInfoOracleList.removeIf(e->!seen.add(getUniqueKeyForGeometryInfo(e)));

private String getUniqueKeyForGeometryInfo(GeometryInfoOracle geometryInfoOracle) {
        return geometryInfoOracle.getKkno()
                + "-" + geometryInfoOracle.getWorkingYear()
                + "-" + geometryInfoOracle.getProjectId()
                + "-" + geometryInfoOracle.getStartKM()
                + "-" + geometryInfoOracle.getEndKM();
    }
---

```
