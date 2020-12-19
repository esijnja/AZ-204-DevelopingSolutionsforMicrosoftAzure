#### Task 3: Obtain an MSAL token

1.  In the **Main** method, perform the following actions:

    1.  Create a new variable named *app* of type **[IPublicClientApplication](https://docs.microsoft.com/dotnet/api/microsoft.identity.client.ipublicclientapplication)**.

    1.  Add the following block of code to build a public client application instance by using the static **[PublicClientApplicationBuilder](https://docs.microsoft.com/dotnet/api/microsoft.identity.client.publicclientapplicationbuilder)** class, and then store it in the *app* variable:

        ```
        app = PublicClientApplicationBuilder
            .Create(_clientId)
            .WithAuthority(AzureCloudInstance.AzurePublic, _tenantId)
            .WithRedirectUri("http://localhost")
            .Build();
        ```

    1.  Add the following block of code to create a new generic string **[List<>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1)** with a single value of **user.read**:

        ```
        List<string> scopes = new List<string> 
        { 
            "user.read" 
        };
        ```

    1.  Create a new variable named *result* of type **[AuthenticationResult](https://docs.microsoft.com/dotnet/api/microsoft.identity.client.authenticationresult)**.

    1.  Add the following block of code to acquire a token interactively and store the output in the *result* variable:

        ```
        result = await app
            .AcquireTokenInteractive(scopes)
            .ExecuteAsync();
        ```

    1.  Render the value of the **[AuthenticationResult.AccessToken](https://docs.microsoft.com/dotnet/api/microsoft.identity.client.authenticationresult.accesstoken)** member to the console:

        ```
        Console.WriteLine($"Token:\t{result.AccessToken}");
        ```

1.  Save the **Program.cs** file.