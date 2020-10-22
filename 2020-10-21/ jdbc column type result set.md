###  jdbc column type result set


[ojdbc - how to see table structure in JDBC? - Stack Overflow](https://stackoverflow.com/questions/19222577/how-to-see-table-structure-in-jdbc "ojdbc - how to see table structure in JDBC? - Stack Overflow")


 

```
 ResultSet rs = stmt.executeQuery("select * from emp");
 ResultSetMetaData rsmd = rs.getMetaData();
 System.out.println("No. of columns : " + rsmd.getColumnCount());
 System.out.println("Column name of 1st column : " + rsmd.getColumnName(1));
 System.out.println("Column type of 1st column : " + rsmd.getColumnTypeName(1));

```
