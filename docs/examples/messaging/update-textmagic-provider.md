using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Messaging messaging = new Messaging(client);

Provider result = await messaging.UpdateTextmagicProvider(
    providerId: "<PROVIDER_ID>",
    name: "<NAME>", // optional
    enabled: false, // optional
    username: "<USERNAME>", // optional
    apiKey: "<API_KEY>", // optional
    from: "<FROM>" // optional
);