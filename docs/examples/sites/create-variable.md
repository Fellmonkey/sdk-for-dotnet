using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Sites sites = new Sites(client);

Variable result = await sites.CreateVariable(
    siteId: "<SITE_ID>",
    key: "<KEY>",
    value: "<VALUE>",
    secret: false // optional
);