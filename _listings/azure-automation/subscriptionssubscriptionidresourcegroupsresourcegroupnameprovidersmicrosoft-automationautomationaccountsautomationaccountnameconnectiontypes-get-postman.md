{
  "info": {
    "name": "Azure Automation API Connection Type List By Automation Account",
    "_postman_id": "123cc013-21cc-4212-9af4-4615c725904c",
    "description": "Retrieve a list of connectiontypes.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "connection",
      "item": [
        {
          "id": "e17cef46-c34e-48c4-9262-12f8be94f89c",
          "name": "ConnectionType_ListByAutomationAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/connectionTypes"
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
            "description": "Retrieve a list of connectiontypes"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2fa03ec3-baec-44a9-bed9-ef8c3a314e14"
            }
          ]
        }
      ]
    }
  ]
}