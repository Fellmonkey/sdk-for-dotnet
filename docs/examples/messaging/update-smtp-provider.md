using Appwrite;
using Appwrite.Enums;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Messaging messaging = new Messaging(client);

Provider result = await messaging.UpdateSmtpProvider(
    providerId: "<PROVIDER_ID>",
    name: "<NAME>", // optional
    host: "<HOST>", // optional
    port: 1, // optional
    username: "<USERNAME>", // optional
    password: "<PASSWORD>", // optional
    encryption: SmtpEncryption.None, // optional
    autoTLS: false, // optional
    mailer: "<MAILER>", // optional
    fromName: "<FROM_NAME>", // optional
    fromEmail: "email@example.com", // optional
    replyToName: "<REPLY_TO_NAME>", // optional
    replyToEmail: "<REPLY_TO_EMAIL>", // optional
    enabled: false // optional
);