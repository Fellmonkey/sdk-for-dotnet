using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Messaging messaging = new Messaging(client);

Provider result = await messaging.CreateMsg91Provider(
    providerId: "<PROVIDER_ID>",
    name: "<NAME>",
    templateId: "<TEMPLATE_ID>", // optional
    senderId: "<SENDER_ID>", // optional
    authKey: "<AUTH_KEY>", // optional
    enabled: false // optional
);