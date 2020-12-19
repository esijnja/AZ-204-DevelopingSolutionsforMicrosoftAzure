#### Task 3: Publish new events

1.  In the **Main** method, perform the following actions:

    1.  Add the following block of code to connect to the Event Grid using the credentials you specified earlier in the lab:

        ```
        TopicCredentials credentials = new TopicCredentials(topicKey);
        EventGridClient client = new EventGridClient(credentials);
        ```
    
    1.  Create a new variable named **events**, of type **List<EventGridEvent>**:

        ```
        List<EventGridEvent> events = new List<EventGridEvent>();
        ```

    1.  Add the following block of code to: create two new variables named **firstPerson** of an anonymous type, and **firstEvent** of type **EventGridEvent**; populate the **EventGridEvent** variable with sample data; and add the **firstEvent** instance to your **events** list:

        ```
        var firstPerson = new
        {
            FullName = "Alba Sutton",
            Address = "4567 Pine Avenue, Edison, WA 97202"
        };    
            
        EventGridEvent firstEvent = new EventGridEvent
        {
            Id = Guid.NewGuid().ToString(),
            EventType = "Employees.Registration.New",
            EventTime = DateTime.Now,
            Subject = $"New Employee: {firstPerson.FullName}",
            Data = firstPerson.ToString(),
            DataVersion = "1.0.0"
        };
        events.Add(firstEvent);
        ```

    1.  Add the following block of code to: create two new variables named **secondPerson** of an anonymous type, and **secondEvent** of type **EventGridEvent**; populate the **EventGridEvent** variable with sample data; and add the **secondEvent** instance to your **events** list:

        ```
        var secondPerson = new
        {
            FullName = "Alexandre Doyon",
            Address = "456 College Street, Bow, WA 98107"
        };

        EventGridEvent secondEvent = new EventGridEvent
        {
            Id = Guid.NewGuid().ToString(),
            EventType = "Employees.Registration.New",
            EventTime = DateTime.Now,
            Subject = $"New Employee: {secondPerson.FullName}",
            Data = secondPerson.ToString(),
            DataVersion = "1.0.0"
        };
        events.Add(secondEvent);
        ```

    1.  Add the following block of code to obtain the **Hostname** from the **topicEndpoint** variable, and then use that hostname as a parameter to the **[EventGridClient.PublishEventsAsync](https://docs.microsoft.com/dotnet/api/microsoft.azure.eventgrid.eventgridclient.publisheventswithhttpmessagesasync)** method invocation:

        ```
        string topicHostname = new Uri(topicEndpoint).Host;
        await client.PublishEventsAsync(topicHostname, events);
        ```

    1.  Render the **Events published** message to the console:

        ```
        Console.WriteLine("Events published");
        ```

1.  Save the **Program.cs** file.

1.  Using a terminal, run the .NET console application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\10\\Solution\\EventPublisher** folder.

1.  Review the success message output from the currently running console application.

1.  Close the current terminal.