#### Task 2: Update the SQL connection string

1.  Open the **AdventureWorks.Web/appsettings.json** file in Visual Studio Code.

1.  Replace the value of the *ConnectionStrings.AdventureWorksSqlContext* property with the **ADO.NET (SQL Authentication) connection string** of the SQL database that you recorded earlier in this lab.
    
    > **Note**: It's important that you use your updated connection string here. The original connection string copied from the portal won't have the username and password necessary to connect to the SQL database.

1.  Save the **appsettings.json** file.