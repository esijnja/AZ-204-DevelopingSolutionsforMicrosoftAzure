#### Task 2: Create an HTTP-triggered function

1. Still in the open command prompt,create a new function with the following details:
    - template: **HTTP trigger**
    - name: **FileParser**

    ```powershell
    func new --template "HTTP trigger" --name "FileParser"
    ```

    > **Note**: You can review the documentation to [create a new function][azure-functions-core-tools-new-function] using the **Azure Functions Core Tools**.
1. Close the currently running **Windows Terminal** application.