#### Task 2: Define a new API

1.  Access the **prodapi*[yourname]*** API Management service instance that you created earlier in this lab.

1.  Create a new **Blank API** with the following details:
    
    -   Display name: **HTTPBin API**

    -   Name: **httpbin-api**

    -   Web service URL: *Enter the URL for the web app that you copied earlier in this lab*

        > **Note**: Depending on how you copy the URL, you might need to add an "http://" prefix to create a valid URL value.

1.  Add a new **operation** to the recently created API with the following details:
    
    -   Display name: **Echo Headers**

    -   Name: **echo-headers**

    -   URL: **GET /**

1.  Add a new **Set Headers** inbound policy to **All Operations** with the following details:
    
    -   Name: **source**
    
    -   Value: **azure-api-mgmt**

    -   Action: **append**

1.  Update the **Backend** for the **Echo Headers** operation by overriding the **Service URL** and appending **/headers** to its current value.

    > **Note**: For example, if the current value is **http://httpapi*[yourname]*.azurewebsites.net**, the new value will be **http://httpapi*[yourname]*.azurewebsites.net/headers**

1.  Test the **Echo Headers** operation in the **HTTPBin API**, observing the results of the API request.

    > **Note**: Observe how there's many headers sent as part of your request that are echoed in the response. Specifically, you'll notice the new **Source** header that you created as part of this task.