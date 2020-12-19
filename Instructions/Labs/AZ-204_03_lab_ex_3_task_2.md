#### Task 2: Modify the Program class to access Storage

1.  Open the **Program.cs** file in Visual Studio Code.

1.  Delete all existing code in the **Program.cs** file.

1.  Add the following **using** directives for libraries that will be referenced by the application:

    ```
    using Azure.Storage;
    using Azure.Storage.Blobs;
    using Azure.Storage.Blobs.Models;
    using System;
    using System.Threading.Tasks;
    ```

1.  Create a new **Program** class with three constant string properties named **blobServiceEndpoint**, **storageAccountName**, and **storageAccountKey**, and then create an asynchronous **Main** entry point method:

    ```
    public class Program
    {
        private const string blobServiceEndpoint = "";
        private const string storageAccountName = "";
        private const string storageAccountKey = "";
        
        public static async Task Main(string[] args)
        {
        }
    }
    ```

1.  Update the **blobServiceEndpoint** string constant by setting its value to the **Primary Blob Service Endpoint** of the storage account that you recorded earlier in this lab.

1.  Update the **storageAccountName** string constant by setting its value to the **Storage account name** of the Storage account that you recorded earlier in this lab.

1.  Update the **storageAccountKey** string constant by setting its value to the **Key** of the Storage account that you recorded earlier in this lab.