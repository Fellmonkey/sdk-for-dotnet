using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Users users = new Users(client);

Preferences result = await users.UpdatePrefs(
    userId: "<USER_ID>",
    prefs: [object]
);