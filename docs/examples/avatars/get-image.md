using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Avatars avatars = new Avatars(client);

byte[] result = await avatars.GetImage(
    url: "https://example.com",
    width: 0, // optional
    height: 0 // optional
);