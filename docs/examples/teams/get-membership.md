using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Teams teams = new Teams(client);

Membership result = await teams.GetMembership(
    teamId: "<TEAM_ID>",
    membershipId: "<MEMBERSHIP_ID>"
);