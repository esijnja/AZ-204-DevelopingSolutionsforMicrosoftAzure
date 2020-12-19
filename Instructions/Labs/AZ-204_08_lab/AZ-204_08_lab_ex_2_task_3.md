#### Task 3: Manipulate an API response

1.  Add a new **operation** to the API with the following details:
    
    -   Display name: **Get Legacy Data**

    -   Name: **get-legacy-data**

    -   URL: **GET /xml**

1.  Test the **Get Legacy Data** operation in the **HTTPBin API**, observing the results of the API request.

    > **Note**: At this point, the results should be in XML format.

1.  Add a new custom outbound policy scoped to the **Get Legacy Data** operation by first locating the following block of XML content:

    ```
    <outbound>
        <base />
    </outbound>
    ```

1.  Replace that block of XML with the following XML, and then save the policy:
    
    ```
    <outbound>
        <base />
        <xml-to-json kind="direct" apply="always" consider-accept-header="false" />
    </outbound>
    ```

1.  Test the **Get Legacy Data** operation in the **HTTPBin API**, observing the results of the API request.

    > **Note**: The new results are in JSON format.

1.  Use the **Trace** feature of the test tool to observe the request sent to the back-end service.

#### Review

In this exercise, you built a proxy tier between your App Service resource and any developers who wish to make queries.