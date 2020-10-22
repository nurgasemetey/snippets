###  jdbc result set get all columns


[java - How do you get values from all columns using ResultSet.getBinaryStream() in jdbc? - Stack Overflow](https://stackoverflow.com/questions/24943894/how-do-you-get-values-from-all-columns-using-resultset-getbinarystream-in-jdbc "java - How do you get values from all columns using ResultSet.getBinaryStream() in jdbc? - Stack Overflow")


 

```
  public static void spitOutAllTableRows(String tableName, Connection conn) {
    try {
      System.out.println("current " + tableName + " is:");
      try (PreparedStatement selectStmt = conn.prepareStatement(
              "SELECT * from " + tableName, ResultSet.TYPE_SCROLL_INSENSITIVE, ResultSet.CONCUR_READ_ONLY);
           ResultSet rs = selectStmt.executeQuery()) {
        if (!rs.isBeforeFirst()) {
          System.out.println("no rows found");
        }
        else {
          while (rs.next()) {
            for (int i = 1; i < rs.getMetaData().getColumnCount() + 1; i++) {
              System.out.print(" " + rs.getMetaData().getColumnName(i) + "=" + rs.getObject(i));
            }
            System.out.println("");
          }
        }
      }
    }
    catch (SQLException e) {
      throw new RuntimeException(e);
    }
  }
```
