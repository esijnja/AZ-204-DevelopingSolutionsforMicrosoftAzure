#### Task 3: Use the Microsoft Graph SDK to query user profile information

1.  Within the **Main** method, remove the following block of unnecessary code:

    ```
    AuthenticationResult result;
        
    result = await app
        .AcquireTokenInteractive(scopes)
        .ExecuteAsync();

    Console.WriteLine($"Token:\t{result.AccessToken}");
    ```

1.  In the **Main** method, perform the following actions:

    1.  Create a new variable named *provider* of type **DeviceCodeProvider** that passes in the variables *app*, and *scopes* as constructor parameters:

        ```
        DeviceCodeProvider provider = new DeviceCodeProvider(app, scopes);
        ```

    1.  Create a new variable named *client* of type **GraphServiceClient** that passes in the variable *provider* as a constructor parameter:

        ```
        GraphServiceClient client = new GraphServiceClient(provider);
        ```

    1.  Add the following block of code to use the **GraphServiceClient** instance to asynchronously get the response of issuing an HTTP request to the relative **/Me** directory of the REST API, and then store the result in a new variable named *myProfile* of type **User**:

        ```
        User myProfile = await client.Me
            .Request()
            .GetAsync();
        ```

    1.  Render the value of the **User.DisplayName** and **User.Id** members to the console:

        ```
        Console.WriteLine($"Name:\t{myProfile.DisplayName}");
        Console.WriteLine($"AAD Id:\t{myProfile.Id}");
        ```

1.  Save the **Program.cs** file.