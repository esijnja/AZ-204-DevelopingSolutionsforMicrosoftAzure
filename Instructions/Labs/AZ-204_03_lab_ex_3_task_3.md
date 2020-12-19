#### Task 3: Connect to the Azure Storage blob service endpoint

1.  In the **Main** method, add the following block of code to connect to the storage account and to retrieve account metadata:

    ```
    StorageSharedKeyCredential accountCredentials = new StorageSharedKeyCredential(storageAccountName, storageAccountKey);

    BlobServiceClient serviceClient = new BlobServiceClient(new Uri(blobServiceEndpoint), accountCredentials);

    AccountInfo info = await serviceClient.GetAccountInfoAsync();
    ```

1.  Still in the **Main** method, add the following block of code to print metadata about the storage account:

    ```
    await Console.Out.WriteLineAsync($"Connected to Azure Storage Account");
    await Console.Out.WriteLineAsync($"Account name:\t{storageAccountName}");
    await Console.Out.WriteLineAsync($"Account kind:\t{info?.AccountKind}");
    await Console.Out.WriteLineAsync($"Account sku:\t{info?.SkuName}");
    ```

1.  Save the **Program.cs** file.

1.  Using a terminal, run the console application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\03\\Solution\\BlobManager** folder.

1.  Observe the output from the currently running console application. The output contains metadata for the Storage account that was retrieved from the service.

1.  Close the current terminal.