#### Task 2: Modify the Program class

1.  Open the **Program.cs** file in Visual Studio Code.

1.  Delete all existing code in the **Program.cs** file.

1.  Add the following **using** directives for libraries that will be referenced by the application:

    ```
    using Microsoft.Identity.Client;
    using System;
    using System.Collections.Generic;
    using System.Threading.Tasks;
    ```

1.  Create a new **Program** class with two constant string properties named **_clientId** and **_tenantId**, and then create an asynchronous **Main** entry point method:

    ```
    public class Program
    {
        private const string _clientId = "<app-reg-client-id>";
        private const string _tenantId = "<aad-tenant-id>";
        
        public static async Task Main(string[] args)
        {
        }
    }
    ```

1.  Update the **_clientId** string constant by setting its value to the **Application (client) ID** that you recorded earlier in this lab.

1.  Update the **_tenantId** string constant by setting its value to the **Directory (tenant) ID** that you recorded earlier in this lab.