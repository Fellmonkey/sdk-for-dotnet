using Appwrite;
using Appwrite.Enums;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Functions functions = new Functions(client);

Execution result = await functions.CreateExecution(
    functionId: "<FUNCTION_ID>",
    body: "<BODY>", // optional
    async: false, // optional
    path: "<PATH>", // optional
    method: ExecutionMethod.GET, // optional
    headers: [object], // optional
    scheduledAt: "" // optional
);