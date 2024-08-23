# JMeter
* It is Open-source testing tool
     1. Add>Thread>Thread Group> To create a user
     2. HTTP Request   > To pass the ip
     3. Http Header Manager > Authorization
     4. View Result Tree > To check the result
     5. Assertions (Response) > Check the response through response code or error message

* CSV data set config > To Handle the dynamic values
     1.Add thread>http request>Add ip>Define parameters (i.e. username,password)
     2.Add CSV data set config> create a csv file>copy file path>paste in filename field+add file name.csv>Define variable name
     3.view results in tree

* Bearer Token Handling -
     1.Add Http Request>Add Login parameters in http request
     2.Add Regular expression Extractor
     3.Add HTTP Header Manager
     4.Add Bean Shell preprocessor
     5.View Result in Tree

* Database Testing using “JDBC Connection configuration"
   -DBC Driver Class: It’s different for every Database vendor
   -Mysql uses com.mysql.jdbc.Driver
   -Oracle uses oracle.jdbc.driver.OracleDriver
   -Microsoft uses com.microsoft.sqlserver.jdbc.SQLServerDriver
  1.Add Thread group
  2.jdbc connection configuration : we will define the database URL, JDBC driver class, the MySQL  username and password, etc.
    -jdbc:sqlserver://[serverName[\instanceName][:portNumber]][;property=value[;property=value]]
    -Variable Name: This value will be used in our JDBC Sampler. In case there is more than one SQL connection, JDBC request will use the right DB Connection by using this value.
    -Connection Pool Configuration: Leave it as it is. These values are good enough for a performance test. In case it’s needed, increasing or decreasing the values is a possibilities.
    -jdbc request : we define the query (Select * from abc)
    -Listener : To check result















