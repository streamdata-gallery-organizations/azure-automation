{
  "info": {
    "name": "Azure Automation API Test Jobs Suspend",
    "_postman_id": "5186bdf3-d723-4ebe-a24e-5e3559d9218c",
    "description": "Suspend the test job.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "test",
      "item": [
        {
          "id": "a4f30b7c-ff6d-4314-a1e0-aab6f4ac19ce",
          "name": "TestJobs_Suspend",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/runbooks/:runbookName/draft/testJob/suspend"
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
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Suspend the test job"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "37c9374f-cb92-4151-a7d4-bdcd7ee721f6"
            }
          ]
        }
      ]
    }
  ]
}