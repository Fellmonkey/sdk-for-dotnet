using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://<REGION>.cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>"); // Your project ID

Functions functions = new Functions(client);

Deployment result = await functions.CreateDeployment(
    functionId: "<FUNCTION_ID>",
    code: InputFile.FromPath("./path-to-files/image.jpg"),
    activate: false,
    entrypoint: "<ENTRYPOINT>", // optional
    commands: "<COMMANDS>" // optional
);