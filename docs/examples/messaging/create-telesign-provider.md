using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Messaging messaging = new Messaging(client);

Provider result = await messaging.CreateTelesignProvider(
    providerId: "<PROVIDER_ID>",
    name: "<NAME>",
    from: "+12065550100", // optional
    customerId: "<CUSTOMER_ID>", // optional
    apiKey: "<API_KEY>", // optional
    enabled: false // optional
);