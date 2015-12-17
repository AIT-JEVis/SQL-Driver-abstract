# SQL-Driver-abstract
Abstract  Genric SQL Data Source Driver for the JEDataCollector 

Common class for all SQL Drivers. Children only need to implement two functions
```
abstract protected String loadJDBC(String host, int port, String schema,
            String domain, String dbUser, String dbPW)
            throws ClassNotFoundException, SQLException;
   
```

and
```
abstract protected String getClassName();
```

`loadJDBC` defines which JDBC driver is loaded and which connection url is used to connect to the server.
`getClassName` defines the JEVis classname for the implemented driver.
