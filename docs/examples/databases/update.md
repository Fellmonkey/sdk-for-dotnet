using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Databases databases = new Databases(client);

Database result = await databases.Update(
    databaseId: "<DATABASE_ID>",
    name: "<NAME>",
    enabled: false // optional
);