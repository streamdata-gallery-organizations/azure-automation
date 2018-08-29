{
  "info": {
    "name": "Azure Automation API Test Jobs Get",
    "_postman_id": "6794a3f4-b90b-4b9b-a231-130cf98e766a",
    "description": "Retrieve the test job for the specified runbook.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "test",
      "item": [
        {
          "id": "cfc673fd-ccf9-4a5f-8688-1fbd676ddcbb",
          "name": "TestJobs_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/runbooks/:runbookName/draft/testJob"
              ],
              "query": [
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
                  "id": "runbookName",
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
            "description": "Retrieve the test job for the specified runbook"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d219bdf6-267c-466d-84bb-b6e9e2790098"
            }
          ]
        }
      ]
    }
  ]
}