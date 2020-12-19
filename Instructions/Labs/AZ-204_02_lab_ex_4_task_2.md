#### Task 2: Observe function code

1. Open **Visual Studio Code**.
1. Using **Visual Studio Code**, open the solution folder found at **Allfiles (F):\\Allfiles\\Labs\\02\\Starter\\func**.
1. Open the **Recurring.cs** file.
1. In the code editor, observe the implementation:

    ```csharp
    using System;
    using Microsoft.Azure.WebJobs;
    using Microsoft.Azure.WebJobs.Host;
    using Microsoft.Extensions.Logging;

    namespace func
    {
        public static class Recurring
        {
            [FunctionName("Recurring")]
            public static void Run([TimerTrigger("0 */5 * * * *")]TimerInfo myTimer, ILogger log)
            {
                log.LogInformation($"C# Timer trigger function executed at: {DateTime.Now}");
            }
        }
    }
    ```