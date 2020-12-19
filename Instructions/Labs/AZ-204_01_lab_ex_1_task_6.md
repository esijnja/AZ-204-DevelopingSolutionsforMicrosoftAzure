#### Task 6: Deploy an ASP.NET web application to Web Apps

1.  Using Visual Studio Code, open the web application in the **Allfiles (F):\\Allfiles\\Labs\\01\\Starter\\API** folder.

1.  Open the **Controllers\\ImagesController.cs** file, and then observe the code in each of the methods.

1.  Open the Windows Terminal application.

1.  Sign in to the Azure CLI by using your Azure credentials:

    ```
    az login
    ```

1.  List all the apps in your **ManagedPlatform** resource group:

    ```
    az webapp list --resource-group ManagedPlatform
    ```

1.  Find the apps that have the **imgapi\*** prefix:

    ```
    az webapp list --resource-group ManagedPlatform --query "[?starts_with(name, 'imgapi')]"
    ```

1.  Print only the name of the single app that has the **imgapi\*** prefix:

    ```
    az webapp list --resource-group ManagedPlatform --query "[?starts_with(name, 'imgapi')].{Name:name}" --output tsv
    ```

1.  Change the current directory to the **Allfiles (F):\\Allfiles\\Labs\\01\\Starter\\API** directory that contains the lab files:

    ```
    cd F:\Allfiles\Labs\01\Starter\API\
    ```

1.  Deploy the **api.zip** file to the web app that you created earlier in this lab:

    ```
    az webapp deployment source config-zip --resource-group ManagedPlatform --src api.zip --name <name-of-your-api-app>
    ```

    > **Note**: Replace the *\<name-of-your-api-app\>* placeholder with the name of the web app that you created earlier in this lab. You recently queried this app’s name in the previous steps.

1.	Access the **imgapi*[yourname]*** web app that you created earlier in this lab. Open the **imgapi*[yourname]*** web app in your browser.

1.	Perform a GET request to the root of the website, and then observe the JavaScript Object Notation (JSON) array that's returned. This array should contain the URL for your single uploaded image in your storage account.

1.  Close the currently running Visual Studio Code and Windows Terminal applications.

#### Review

In this exercise, you created a web app in Azure and then deployed your ASP.NET web application to Web Apps by using the Azure CLI and the Kudu zip file deployment utility.