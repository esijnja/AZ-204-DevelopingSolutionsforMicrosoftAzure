#### Task 1: Deploy an application to the web app

1.  Open Visual Studio Code.

1.  In Visual Studio Code, open the **Allfiles (F):\\Allfiles\\Labs\\12\\Starter\\Api** folder.

1.  Use the Explorer in Visual Studio Code to open a new terminal with the context set to the current working directory.

1.  Sign in to the Azure Command-Line Interface (CLI) by using your Azure credentials:

    ```
    az login
    ```

1.  List all the apps in your **MonitoredAssets** resource group:
    
    ```
    az webapp list --resource-group MonitoredAssets
    ```

1.  Find the apps that have the prefix **smpapi\***:
    
    ```
    az webapp list --resource-group MonitoredAssets --query "[?starts_with(name, 'smpapi')]"
    ```

1.  Print only the name of the single app that has the prefix **smpapi\***:

    ```
    az webapp list --resource-group MonitoredAssets --query "[?starts_with(name, 'smpapi')].{Name:name}" --output tsv
    ```

1.  Change the current directory to the **Allfiles (F):\\Allfiles\\Labs\\12\\Starter** directory that contains the lab files:

    ```
    cd F:\Allfiles\Labs\12\Starter\
    ```

1.  Deploy the **api.zip** file to the web app that you created earlier in this lab:

    ```
    az webapp deployment source config-zip --resource-group MonitoredAssets --src api.zip --name <name-of-your-api-app>
    ```

    > **Note**: Replace the *name-of-your-api-app* placeholder with the name of the web app that you created earlier in this lab. You recently queried this app’s name in the previous steps.

1.  Return to your currently open browser window that's displaying the Azure portal.

1.  Access the ***smpapi\***[yourname]*** web app that you created earlier in this lab.

1.  Open the ***smpapi\***[yourname]*** web app in your browser.

1.  Perform a GET request to the **/weatherforecast** relative path of the website, and then find the JavaScript Object Notation (JSON) array that's returned as a result of using the API.

    > **Note**: For example, if your URL is https://smpapistudent.azurewebsites.net, the new URL would be https://smpapistudent.azurewebsites.net/weatherforecast.