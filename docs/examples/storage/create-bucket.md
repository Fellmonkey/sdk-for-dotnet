using Appwrite;
using Appwrite.Enums;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Storage storage = new Storage(client);

Bucket result = await storage.CreateBucket(
    bucketId: "<BUCKET_ID>",
    name: "<NAME>",
    permissions: ["read("any")"], // optional
    fileSecurity: false, // optional
    enabled: false, // optional
    maximumFileSize: 1, // optional
    allowedFileExtensions: new List<string>(), // optional
    compression: .None, // optional
    encryption: false, // optional
    antivirus: false // optional
);