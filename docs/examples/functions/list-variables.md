using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Functions functions = new Functions(client);

VariableList result = await functions.ListVariables(
    functionId: "<FUNCTION_ID>"
);