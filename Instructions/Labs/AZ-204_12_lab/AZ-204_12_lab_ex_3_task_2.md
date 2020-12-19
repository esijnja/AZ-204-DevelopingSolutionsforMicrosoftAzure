#### Task 2: Configure in-depth metric collection for Web Apps

1.  Return to your currently open browser window that's displaying the Azure portal.

1.  Access the ***smpapi\***[yourname]*** web app that you created earlier in this lab.

1.  Go to the **Application Insights** configuration section.

1.  **Enable** Application Insights instrumentation for **.NET** by using the following settings:

    -   Collection level: **Recommended**

    -   Profiler: **On**

    -   Snapshot debugger: **Off**

    -   SQL Commands: **Off**

1.  Save your Application Insights instrumentation configuration.

1.  Open the ***smpapi\***[yourname]*** web app in your browser.

1.  Perform a GET request to the **/weatherforecast** relative path of the website, and then observe the JSON array that's returned as a result of using the API.

    > **Note**: For example, if your URL is https://smpapistudent.azurewebsites.net, the new URL would be https://smpapistudent.azurewebsites.net/weatherforecast.

1.  Record the URL that you used to access the JSON array.

    > **Note**: Using the example from the previous step, you would record the URL ``https://smpapistudent.azurewebsites.net/weatherforecast``.