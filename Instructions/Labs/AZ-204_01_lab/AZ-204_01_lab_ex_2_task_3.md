#### Task 3: Deploy an ASP.NET web application to Web Apps

1.  Using Visual Studio Code, open the web application in the **Allfiles (F):\\Allfiles\\Labs\\01\\Starter\\Web** folder.

1.  Open the **Pages\\Index.cshtml.cs** file, and then observe the code in each of the methods.

1.  Open the Windows Terminal application, and then sign in to the Azure CLI by using your Azure credentials:

    ```
    az login
    ```

1.  List all the apps in your **ManagedPlatform** resource group:

    ```
    az webapp list --resource-group ManagedPlatform
    ```

1.  Find the apps that have the **imgweb\*** prefix:

    ```
    az webapp list --resource-group ManagedPlatform --query "[?starts_with(name, 'imgweb')]"
    ```

1.  Print only the name of the single app that has the **imgweb\*** prefix:
    
    ```
    az webapp list --resource-group ManagedPlatform --query "[?starts_with(name, 'imgweb')].{Name:name}" --output tsv
    ```

1.  Change your current directory to the **Allfiles (F):\\Allfiles\\Labs\\01\\Starter\\Web** directory that contains the lab files:

    ```
    cd F:\Allfiles\Labs\01\Starter\Web\
    ```
    
1.  Deploy the **web.zip** file to the web app that you created earlier in this lab:

    ```
    az webapp deployment source config-zip --resource-group ManagedPlatform --src web.zip --name <name-of-your-web-app>
    ```

    > **Note**: Replace the *\<name-of-your-web-app\>* placeholder with the name of the web app that you created earlier in this lab. You recently queried this app’s name in the previous steps.
    
1.  Access the **imgweb*[yourname]*** web app that you created earlier in this lab. Open the **imgweb*[yourname]*** web app in your browser.

1.	From the **Contoso Photo Gallery** webpage, find the **Upload a new image** section, and then upload the **bahnmi.jpg** file in the **Allfiles (F):\\Allfiles\\Labs\\01\\Starter\\Images** folder on your lab machine.

    > **Note**: Ensure you click the **Upload** button to upload the image to Azure.

1.	Observe that the list of gallery images has updated with your new image.

    > **Note**: In some rare cases, you might need to refresh your browser window to retrieve the new image.

1.  Close the currently running Visual Studio Code and Windows Terminal applications.

#### Review

In this exercise, you created an Azure web app and deployed an existing web application’s code to the resource in the cloud.