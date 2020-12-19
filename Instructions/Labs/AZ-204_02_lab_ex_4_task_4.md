#### Task 4: Update the function integration configuration

1. Open **Visual Studio Code**.
1. Using **Visual Studio Code**, open the solution folder found at **Allfiles (F):\\Allfiles\\Labs\\02\\Starter\\func**.
1. Open the **Recurring.cs** file.
1. In the code editor, update the **Run** method signature to change the schedule to execute once every **30 seconds**:

    ```csharp
    [FunctionName("Recurring")]
    public static void Run([TimerTrigger("*/30 * * * * *")]TimerInfo myTimer, ILogger log)
    ```

1. **Save** the **Recurring.cs** file.