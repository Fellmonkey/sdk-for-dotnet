using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Messaging messaging = new Messaging(client);

SubscriberList result = await messaging.ListSubscribers(
    topicId: "<TOPIC_ID>",
    queries: new List<string>(), // optional
    search: "<SEARCH>" // optional
);