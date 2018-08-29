{
  "info": {
    "name": "Azure Automation API Dsc Compilation Job List By Automation Account",
    "_postman_id": "e6eb409e-538e-441c-8da3-d3b30153dd13",
    "description": "Retrieve a list of dsc compilation jobs.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "dsc",
      "item": [
        {
          "id": "4c4be095-0bb8-433a-b2fa-6c4c881a940e",
          "name": "DscCompilationJob_ListByAutomationAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/compilationjobs"
              ],
              "query": [
                {
                  "key": "$filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "automationAccountName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                },
                {
                  "id": "resourceGroupName",
                  "value": "resourceGroupName",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a list of dsc compilation jobs"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8515bbc2-b75c-4d8b-8809-4521ce901282"
            }
          ]
        }
      ]
    }
  ]
}