using Appwrite;
using Appwrite.Enums;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Users users = new Users(client);

User result = await users.CreateSHAUser(
    userId: "<USER_ID>",
    email: "email@example.com",
    password: "password",
    passwordVersion: PasswordHash.Sha1, // optional
    name: "<NAME>" // optional
);