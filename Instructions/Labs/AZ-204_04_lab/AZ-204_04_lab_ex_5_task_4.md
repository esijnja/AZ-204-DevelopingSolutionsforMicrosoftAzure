#### Task 4: Update .NET application startup logic

1.  Open the **AdventureWorks.Web/Startup.cs** file in Visual Studio Code.

1.  In the **Startup** class, find the existing **ConfigureProductService** method.

    > **Note**: The current product service uses SQL as its database.

1.  Replace the **ConfigureProductService** method with the following code:

    ```
    public void ConfigureProductService(IServiceCollection services)
    {
        services.AddScoped<IAdventureWorksProductContext, AdventureWorksCosmosContext>(provider =>
                new AdventureWorksCosmosContext(
                    _configuration.GetConnectionString(nameof(AdventureWorksCosmosContext))
                )
        );
    }
    ```

1.  Save the **Startup.cs** file.