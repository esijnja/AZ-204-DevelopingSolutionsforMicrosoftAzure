#### Task 2: Write .NET code to connect to Azure Cosmos DB

1.  Create a new **AdventureWorks.Context/AdventureWorksCosmosContext.cs** file in Visual Studio Code.

1.  Add the following **using** directives for libraries that will be referenced by the application:

    ```
    using AdventureWorks.Models;
    using Microsoft.Azure.Cosmos;
    using Microsoft.Azure.Cosmos.Linq;
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Threading.Tasks;
    ```
    
1.  Enter the following code to add an **AdventureWorks.Context** namespace block:

    ```
    namespace AdventureWorks.Context
    {
    }
    ```

1.  Create a new **AdventureWorksCosmosContext** class that implements the **IAdventureWorksProductContext** interface with a single read-only *Container* variable:

    ```
    public class AdventureWorksCosmosContext : IAdventureWorksProductContext
    {
        private readonly Container _container;
    }
    ```

1.  Within the **AdventureWorksCosmosContext** class, add a new constructor that creates a new instance of the **CosmosClient** class, and then obtain both a **Database** and **Container** instance from the client:

    ```
    public AdventureWorksCosmosContext(string connectionString, string database = "Retail", string container = "Online")
    {
        _container = new CosmosClient(connectionString)
            .GetDatabase(database)
            .GetContainer(container);
    }
    ```

1.  Within the **AdventureWorksCosmosContext** class, add a new **FindModelAsync** method that creates a LINQ query, transforms it into an iterator, iterates over the result set, and then returns the single item in the result set:

    ```
    public async Task<Model> FindModelAsync(Guid id)
    {
        var iterator = _container.GetItemLinqQueryable<Model>()
            .Where(m => m.id == id)
            .ToFeedIterator<Model>();

        List<Model> matches = new List<Model>();
        while (iterator.HasMoreResults)
        {
            var next = await iterator.ReadNextAsync();
            matches.AddRange(next);
        }

        return matches.SingleOrDefault();
    }
    ```

1.  Within the **AdventureWorksCosmosContext** class, add a new **GetModelsAsync** method that runs an SQL query, gets the query result iterator, iterates over the result set, and then returns the union of all results:

    ```
    public async Task<List<Model>> GetModelsAsync()
    {
        string query = $@"SELECT * FROM items";

        var iterator = _container.GetItemQueryIterator<Model>(query);

        List<Model> matches = new List<Model>();
        while (iterator.HasMoreResults)
        {
            var next = await iterator.ReadNextAsync();
            matches.AddRange(next);
        }

        return matches;
    }
    ```

1.  Within the **AdventureWorksCosmosContext** class, add a new **FindProductAsync** method that runs an SQL query, gets the query result iterator, iterates over the result set, and then returns the single item in the result set:

    ```
    public async Task<Product> FindProductAsync(Guid id)
    {
        string query = $@"SELECT VALUE products
                            FROM models
                            JOIN products in models.Products
                            WHERE products.id = '{id}'";

        var iterator = _container.GetItemQueryIterator<Product>(query);

        List<Product> matches = new List<Product>();
        while (iterator.HasMoreResults)
        {
            var next = await iterator.ReadNextAsync();
            matches.AddRange(next);
        }

        return matches.SingleOrDefault();
    }
    ```

1.  Save the **AdventureWorksCosmosContext.cs** file.

1.  Using a terminal, change your context to the **AdventureWorks.Context** folder:

    ```
    cd .\AdventureWorks.Context\
    ```
    
1.  Using the same terminal, build the ASP.NET web application project:

    ```
    dotnet build
    ```

    > **Note**: If there are any build errors, review the **AdventureWorksCosmosContext.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\04\\Solution\\AdventureWorks\\AdventureWorks.Context** folder.

1.  Close the current terminal.