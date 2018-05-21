{
  "info": {
    "name": "Azure Automation API Hybrid Runbook Worker Group List By Automation Account",
    "_postman_id": "d8554d53-f64c-4aa9-ba1e-ff1ccef94e56",
    "description": "Retrieve a list of hybrid runbook worker groups.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "hybrid",
      "item": [
        {
          "id": "0eba8206-00d8-4c85-8752-c6055a7dec53",
          "name": "HybridRunbookWorkerGroup_ListByAutomationAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/hybridRunbookWorkerGroups"
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
            "description": "Retrieve a list of hybrid runbook worker groups"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "533c2913-1243-442f-83a0-fca0f24cde6c"
            }
          ]
        }
      ]
    }
  ]
}