# Getting started with Symxify

This guide will strictly walk you through getting started with [Managed Symxify](https://memberwise.io/products/symxify). Documentation for self hosting is available on the [symxify](https://github.com/memberwise/symxify) repository.

### To get started...

To get started with Managed Symxify, you must contact us via our contact form. Accounts cannot be created independently (yet, this will change in the future). You can contact us at [https://memberwise.io/contact](https://memberwise.io/contact). We'll schedule a call and work on provide you with an account to log into. From there, you're freely able to configure Symxify how you please.

### Your Dashboard

Once you login, you'll be sent to your dashboard page. The dashboard page contains some preview information about your tenants users, billing alerts, and any alerts with your Symxify connections.

![alt text](/assets/image3.png)

### Creating a Connection

To create a Symxify connection, click on the "Symxify Connection" card. This will take you to the Symxify connections page, where you can view and modify your Symxify connections.

Click "Create New Connection" to go to the create connection page.

Fill out the fields in the create connection page.

| Field                          | Description                                                                                                                                                                                                                              |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Symitar SymXchange URL         | The base URL of your symxchange connection. Do not include HTTPS or any trailing slashes. (e.g., symitar123.host.net)                                                                                                                    |
| Symitar SymXchange Port        | The port number to access this SyXchange connection                                                                                                                                                                                      |
| Symitar SymXchange Certificate | The certificate contents used to authenticate yourself to your SymXchange client.                                                                                                                                                        |
| Symxify Connection Name        | A descriptive name for your Symxify connection.                                                                                                                                                                                          |
| Symxify Connection Description | The description of your connection.                                                                                                                                                                                                      |
| Connection Type                | The type of Symxify connection. This can be Development, Staging or Production. Development and staging connections do not alert or perform health checks. Production connections will alert and perform health checks every 15 minutes. |
| Symxify Key                    | The secret key of your symxify connection. This should be stored like a private key. This key cannot be inspected once the connection is created, so keep it in a secure place.                                                          |
| Service Version                | The version of SymXchange you'd like to interact with. The only supported version is CRUD.                                                                                                                                               |

![alt text](/assets/image4.png)

Once the fields are filled out, click the "Create Connection" button at the top of the page.

### Testing your connection

Once you've created a connection, you can test it at any time by clicking the "Test Connection" button at the top of the page.

You will need to whitelist the IP address [209.71.81.74](209.71.81.74), which is the static egress IP for the application. The test will attempt to read a dummy account with a incorrect device information and an administrative password. So long as the server receives some SOAP back, the connection itself is declared as "OK". If the server receives any HTTP error or is unable to reach the Symxchange server, the connection is declared as "BAD". If your connection fails, you will see the most recent error message at the top of the page. You can also view the logs in the Symxify Logs page to view all connection attempts.

### Building with Symxify

Once you're successfully tested your connection, you're ready to build!

There are two official clients for using Symxify.

| Client                                                                                            | Description                                                                                                                                                     |
| ------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [symxify-client (typescript)](https://github.com/memberwise/symxify/tree/main/clients/typescript) | Our official TypeScript client. The client is compatible with all TypeScript products (e.g., React, Angular, Vue)                                               |
| [Symxify.Client (.NET)   ](https://github.com/memberwise/symxify/tree/main/clients/c%23)                  | Our official C# client. The client is compatible with .NET 9 + and supports all the modern features of C#, such as dependency injection and easy configuration. |
