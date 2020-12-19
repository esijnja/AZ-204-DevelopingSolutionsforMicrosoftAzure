#### Task 2: Modify the Program class to connect to Event Grid

1.  Open the **Program.cs** file in Visual Studio Code.

1.  Delete all existing code in the **Program.cs** file.

1.  Add the following **using** directives for libraries that the application will reference:

    ```
    using Microsoft.Azure.EventGrid;
    using Microsoft.Azure.EventGrid.Models;
    using System;
    using System.Collections.Generic;
    using System.Threading.Tasks;
    ```

1.  Create a new **Program** class with two constant string properties named **topicEndpoint** and **topicKey**, and then create an asynchronous **Main** entry point method:

    ```
    public class Program
    {
        private const string topicEndpoint = "";
        private const string topicKey = "";
        
        public static async Task Main(string[] args)
        {
        }
    }
    ```

1.  Update the **topicEndpoint** string constant by setting its value to the **Topic Endpoint** of the Event Grid topic that you recorded earlier in this lab.

1.  Update the **topicKey** string constant by setting its value to the **Key** of the Event Grid topic that you recorded earlier in this lab.