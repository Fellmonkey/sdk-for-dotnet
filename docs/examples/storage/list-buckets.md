using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Storage storage = new Storage(client);

BucketList result = await storage.ListBuckets(
    queries: new List<string>(), // optional
    search: "<SEARCH>" // optional
);