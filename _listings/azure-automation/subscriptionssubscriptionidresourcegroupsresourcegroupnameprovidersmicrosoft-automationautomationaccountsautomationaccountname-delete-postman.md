{
  "info": {
    "name": "Azure Automation API Automation Account Delete",
    "_postman_id": "488ae629-49d7-4b3d-88ac-1a4c667f6192",
    "description": "Delete an automation account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "automation",
      "item": [
        {
          "id": "5dd5e6b6-9cd2-446a-aaa7-444f1e279889",
          "name": "AutomationAccount_Delete",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName"
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete an automation account"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "254ceaa6-2968-49dd-8447-5cfbc4701da6"
            }
          ]
        }
      ]
    }
  ]
}