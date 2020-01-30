JDBC API is defined in the following packages
-	java.sql and javax.sql
Key classes
-	java.sql.DriverManager
-	java.sql.Connection
-	java.sql.Statement
-	java.sql.ResultSet
-	javax.sql.DataSource (for connection pooling)
Development Process
1.	Get a connection to database
2.	Create a Statement object
3.	Execute SQL query
4.	Process Result Set

Step 1: Get a Connection to Database
Basic syntax
Jdbc:<driver protocol>:<driver connection details>

Examples
MS SQL Server: jdbc:odbc:DemoDSN
Oracle: jdbc:oracle:thin@myserver:1521:demodb
MySQL: jdbc:mysql://localhost:3306/demodb

MySQL:






Failure to connect will throw an exception:
-	Java.sql.SQLException: bad url or credentials
-	Java.lang.ClassNotFoundException: JDBC driver not in classpath

Step 2: Create a Statement object
-	The statement object is based on connection 
o	It will be used later to execute SQL query









Step 3: Execute SQL Query
-	Pass in your SQL query









Step 4: Process the Result Set
-	Result Set is initially placed before first row
-	Method: ResultSet.next()
o	Moves forward one row
o	Returns true if there are more rows to process
-	Looping through a result set







-	Collection of methods for reading data
o	getXXX(columnName)
o	getXXX(columnIndex) one-based

