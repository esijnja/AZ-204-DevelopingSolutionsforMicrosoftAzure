#### Task 2: Update application code to disable HTTPS and use Application Insights

1.  Use the Explorer in Visual Studio Code to open the **Startup.cs** file in the editor.

1.  Find and delete the following line of code at line 39:

    ```
    app.UseHttpsRedirection();
    ```

    > **Note**: This line of code forces the web app to use HTTPS. For this lab, this is unnecessary.

1.  In the **Startup** class, add a new static string constant named **INSTRUMENTATION_KEY** with its value set to the instrumentation key that you copied from the Application Insights resource you created earlier in this lab:

    ```
    private static string INSTRUMENTATION_KEY = "{your_instrumentation_key}";
    ```

    > **Note**: For example, if your instrumentation key is ``d2bb0eed-1342-4394-9b0c-8a56d21aaa43``, your line of code would be ``private static string INSTRUMENTATION_KEY = "d2bb0eed-1342-4394-9b0c-8a56d21aaa43";``

1.  Add a new line of code in the **ConfigureServices** method to configure Application Insights using the provided instrumentation key:

    ```
    services.AddApplicationInsightsTelemetry(INSTRUMENTATION_KEY);
    ```

1.  Save the **Startup.cs** file.

1.  If it's not already open, use the Explorer in Visual Studio Code to open a new terminal with the context set to the current working directory.

1.  Build the .NET web app:

    ```
    dotnet build
   