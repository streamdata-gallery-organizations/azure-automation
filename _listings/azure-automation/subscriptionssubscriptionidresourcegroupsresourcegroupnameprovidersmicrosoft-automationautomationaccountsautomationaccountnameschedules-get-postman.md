{
  "info": {
    "name": "Azure Automation API Schedule List By Automation Account",
    "_postman_id": "e705e567-d9d9-48ca-b98e-6b669b688c29",
    "description": "Retrieve a list of schedules.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "schedule",
      "item": [
        {
          "id": "18f0e289-a9a8-4715-b751-bc4cf139879a",
          "name": "Schedule_ListByAutomationAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/schedules"
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
            "description": "Retrieve a list of schedules"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e5ac5c24-6618-4419-92cc-b2b6b4291a9f"
            }
          ]
        }
      ]
    }
  ]
}