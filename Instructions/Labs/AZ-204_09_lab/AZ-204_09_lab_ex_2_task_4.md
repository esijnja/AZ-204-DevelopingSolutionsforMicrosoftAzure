#### Task 4: Build an HTTP response action

1.  In the **Designer** area, add a new **Response (Request)** action with the following details:
    
    -   Status Code: **200**
    
    -   Body: **Output (Select)**

1.  **Save** the workflow.

#### Review

In this exercise, you built a basic workflow that starts when it's triggered by an HTTP GET request. It then queries a storage service, enumerates the results, and then returns those results as an HTTP response.