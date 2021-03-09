### mongodb serverstatus unauthorized


[mongodb - db.serverStatus() got not authorized on admin to execute command - Database Administrators Stack Exchange](https://dba.stackexchange.com/questions/121832/db-serverstatus-got-not-authorized-on-admin-to-execute-command/121838 "mongodb - db.serverStatus() got not authorized on admin to execute command - Database Administrators Stack Exchange")


 

```
db.grantRolesToUser(
  "admin",
   [
     { role: "clusterMonitor", db:"admin"} 
   ]
);
```
