using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Messaging messaging = new Messaging(client);

Topic result = await messaging.CreateTopic(
    topicId: "<TOPIC_ID>",
    name: "<NAME>",
    subscribe: ["any"] // optional
);