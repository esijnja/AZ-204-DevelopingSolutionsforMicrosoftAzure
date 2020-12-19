#### Task 2: Create and test a .NET application

1.  In the graphical editor, open the **Program.cs** file and replace its contents with the following code, and then save the file:

    ```
    public class Program
    {
        public static void Main(string[] args)
        {        
            // Check if network is available
            if (System.Net.NetworkInformation.NetworkInterface.GetIsNetworkAvailable())
            {
                System.Console.WriteLine("Current IP Addresses:");

                // Get host entry for current hostname
                string hostname = System.Net.Dns.GetHostName();
                System.Net.IPHostEntry host = System.Net.Dns.GetHostEntry(hostname);
                
                // Iterate over each IP address and render their values
                foreach(System.Net.IPAddress address in host.AddressList)
                {
                    System.Console.WriteLine($"\t{address}");
                }
            }
            else
            {
                System.Console.WriteLine("No Network Connection");
            }
        }
    }
    ```

1.  Use the **dotnet run** command at the command prompt to run the application and validate that it finds one or more IP addresses.

1.  Open the **Dockerfile** file in the graphical editor, replace its contents with the following code, and then save the file:

    ```
    # Start using the .NET Core 2.2 SDK container image
    FROM mcr.microsoft.com/dotnet/core/sdk:2.2-alpine AS build

    # Change current working directory
    WORKDIR /app

    # Copy existing files from host machine
    COPY . ./

    # Publish application to the "out" folder
    RUN dotnet publish --configuration Release --output out

    # Start container by running application DLL
    ENTRYPOINT ["dotnet", "out/ipcheck.dll"]
    ```

1.  Close the Cloud Shell pane.