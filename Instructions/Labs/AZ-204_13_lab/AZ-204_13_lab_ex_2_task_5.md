#### Task 5: Create Content Delivery Network endpoints

1.  Access the **contentdeliverynetwork** CDN profile that you created earlier in this lab, and then select **+ Endpoint**.

1.  Add a new endpoint with the following properties:

    -   Name: **cdnmedia*[yourname]***

    -   Origin type: **Storage**

    -   Origin hostname: **contenthost*[yourname]*.blob.core.windows.net** (the Storage account that you created earlier in this lab)

    -   Origin path: **/media**

    -   Optimized for: **General web delivery**

    > **Note**: Wait for Azure to finish creating the CDN endpoint before you move forward with the lab. You'll receive a notification when the account is created.

1.  Add a new endpoint with the following properties:

    -   Name: **cdnvideo*[yourname]***

    -   Origin type: **Storage**

    -   Origin hostname: **contenthost*[yourname]*.blob.core.windows.net** (the Storage account that you created earlier in this lab)

    -   Origin path: **/video**

    -   Optimized for: **Video on demand media streaming**

    > **Note**: Wait for Azure to finish creating the CDN endpoint before you move forward with the lab. You'll receive a notification when the account is created.

1.  Add a new endpoint with the following properties:

    -   Name: **cdnweb*[yourname]***

    -   Origin type: **Web App**

    -   Origin hostname: **landingpage*[yourname]*.azurewebsites.net** (the Web App that you created earlier in this lab)

    -   Optimized for: **General web delivery**

    > **Note**: Wait for Azure to finish creating the CDN endpoint before you move forward with the lab. You'll receive a notification when the account is created.

#### Review

In this exercise, you registered the resource provider for Content Delivery Network and then used the provider to create both CDN profile and endpoint resources.