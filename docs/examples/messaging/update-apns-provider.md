using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Messaging messaging = new Messaging(client);

Provider result = await messaging.UpdateApnsProvider(
    providerId: "<PROVIDER_ID>",
    name: "<NAME>", // optional
    enabled: false, // optional
    authKey: "<AUTH_KEY>", // optional
    authKeyId: "<AUTH_KEY_ID>", // optional
    teamId: "<TEAM_ID>", // optional
    bundleId: "<BUNDLE_ID>", // optional
    sandbox: false // optional
);