#### Task 2: Create new subscription

1.  Access the **hrtopic*[yourname]*** Event Grid topic that you created earlier in this lab.

1.  Create a new **Event Subscription** with the following details:
    
    -   Name: **basicsub**

    -   Event Schema: **Event Grid Schema**

    -   Endpoint Type: **Web Hook**

    -   Endpoint: ***Web App URL recorded earlier in the lab, with an *https://* prefix and an */api/updates* suffix**

        > **Note**: For example, if your **Web App URL** value is **http://eventviewerstudent.azurewebsites.net/**, then your endpoint would be **https://eventviewerstudent.azurewebsites.net/api/updates**.
  
    > **Note**: Wait for Azure to finish creating the subscription before you continue with the lab. You'll receive a notification when the app is created.