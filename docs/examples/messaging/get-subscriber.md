using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Messaging messaging = new Messaging(client);

Subscriber result = await messaging.GetSubscriber(
    topicId: "<TOPIC_ID>",
    subscriberId: "<SUBSCRIBER_ID>"
);