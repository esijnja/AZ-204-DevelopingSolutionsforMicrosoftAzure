#### Task 2: Create a .NET class 

1.  Open the **AdventureWorks.Migrate/Program.cs** file in Visual Studio Code.

1.  Delete all existing code in the **Program.cs** file.

1.  Add the following **using** directives for libraries that will be referenced by the application:

    ```
    using AdventureWorks.Context;
    using AdventureWorks.Models;
    using Microsoft.Azure.Cosmos;
    using Microsoft.EntityFrameworkCore;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Threading.Tasks;
    ```

1.  Create a new **Program** class with two constant string properties and an asynchronous **Main** entry point method:

    ```
    public class Program
    {
        private const string sqlDBConnectionString = "";
        private const string cosmosDBConnectionString = "";
        
        public static async Task Main(string[] args)
        {
        }
    }
    ```

1.  Update the **sqlDBConnectionString** string constant by setting its value to the **ADO.NET (SQL Authentication) connection string** of the SQL database that you recorded earlier in this lab.

    > **Note**: It's important that you use your updated connection string here. The original connection string copied from the portal won't have the username and password necessary to connect to the SQL database.

1.  Update the **cosmosDBConnectionString** string constant by setting its value to the **PRIMARY CONNECTION STRING** of the Azure Cosmos DB account that you recorded earlier in this lab.