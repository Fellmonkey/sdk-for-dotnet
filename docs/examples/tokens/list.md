using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Tokens tokens = new Tokens(client);

ResourceTokenList result = await tokens.List(
    bucketId: "<BUCKET_ID>",
    fileId: "<FILE_ID>",
    queries: new List<string>() // optional
);