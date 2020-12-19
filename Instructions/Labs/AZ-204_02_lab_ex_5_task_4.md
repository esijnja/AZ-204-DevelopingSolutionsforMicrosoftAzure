#### Task 4: Test the Blob-inputted function by using httprepl

1. Open the **Windows Terminal** application.
1. Change the current directory to the **Allfiles (F):\\Allfiles\\Labs\\02\\Starter\\func** project directory.
1. Start the function app project:
    > **Note**: You can review the documentation to [start the function app project locally][azure-functions-core-tools-start-function] using the **Azure Functions Core Tools**.
1. Open a new instance of the **Windows Terminal** application.
1. Start the **httprepl** tool, and then set the base URI to ``http://localhost:7071``:

    ```powershell
    httprepl http://localhost:7071
    ```

    > **Note**: An error message is displayed by the httprepl tool. This message occurs because the tool is searching for a Swagger definition file to use to "traverse" the API. Because your functio projectp does not produce a Swagger definition file, you'll need to traverse the API manually.

1. When you receive the tool prompt, browse to the relative **api/getsettinginfo** endpoint:

    ```powershell
    cd api
    cd getsettinginfo
    ```

1. Run the **get** command for the current endpoint:

    ```powershell
    get
    ```

1. Observe the JSON content of the response from the function app.

1. Exit the **httprepl** application:

    ```powershell
    exit
    ```

1. Close all currently running instances of the **Windows Terminal** application.

> **Review**: In this exercise, you created a function that returns the content of a JSON file in Storage.