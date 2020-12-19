#### Task 2: Write code to access Azure Storage

1.  Open the **Program.cs** file in Visual Studio Code.

1.  Delete all existing code in the **Program.cs** file.

1.  Add the following **using** directives for libraries that will be referenced by the application:

    ```
    using Azure;
    using Azure.Storage.Queues;
    using Azure.Storage.Queues.Models;
    using System;
    using System.Threading.Tasks;
    ```

1.  Create a new **Program** class with two constant string properties named **storageConnectionString** and **messagequeue**, and then create an asynchronous **Main** entry point method:

    ```
    public class Program
    {
        private const string storageConnectionString = "<storage-connection-string>";
        private const string queueName = "messagequeue";

        public static async Task Main(string[] args)
        {
        }
    }
    ```

1.  Update the **storageConnectionString** string constant by setting its value to the **Connection string** of the storage account that you recorded earlier in this lab.