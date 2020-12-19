#### Task 4: Insert items into Azure Cosmos DB

1.  Still within the **Main** method, add the following blocks of code to import the in-memory model and product data as documents to Azure Cosmos DB:

    ```
    using CosmosClient client = new CosmosClient(cosmosDBConnectionString);

    Database database = await client.CreateDatabaseIfNotExistsAsync("Retail");

    Container container = await database.CreateContainerIfNotExistsAsync("Online",
        partitionKeyPath: $"/{nameof(Model.Category)}",
        throughput: 1000
    );

    int count = 0;
    foreach (var item in items)
    {
        ItemResponse<Model> document = await container.UpsertItemAsync<Model>(item);
        await Console.Out.WriteLineAsync($"Upserted document #{++count:000} [Activity Id: {document.ActivityId}]");
    }

    await Console.Out.WriteLineAsync($"Total Azure Cosmos DB Documents: {count}");
    ```

1.  Save the **Program.cs** file.

1.  Using a terminal, change your context to the **AdventureWorks.Migrate** folder:

    ```
    cd .\AdventureWorks.Migrate\
    ```

1.  Using the same terminal, build the .NET console application project:

    ```
    dotnet build
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\04\\Solution\\AdventureWorks\\AdventureWorks.Migrate** folder.