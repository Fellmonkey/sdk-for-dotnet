using Appwrite;
using Appwrite.Enums;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Databases databases = new Databases(client);

UsageDatabase result = await databases.GetDatabaseUsage(
    databaseId: "<DATABASE_ID>",
    range: DatabaseUsageRange.TwentyFourHours // optional
);