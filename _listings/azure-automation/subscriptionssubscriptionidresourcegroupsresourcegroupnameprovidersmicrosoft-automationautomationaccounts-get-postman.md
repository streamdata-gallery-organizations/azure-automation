{
  "info": {
    "name": "Azure Automation API Automation Account List By Resource Group",
    "_postman_id": "6eef3531-9124-45b5-9399-c43ba029110a",
    "description": "Retrieve a list of accounts within a given resource group.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "automation",
      "item": [
        {
          "id": "ac1c641d-0f0f-48b2-bea4-f815e473e08c",
          "name": "AutomationAccount_ListByResourceGroup",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts"
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
            "description": "Retrieve a list of accounts within a given resource group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8a19415b-4311-438b-b7c7-bd29346c0283"
            }
          ]
        }
      ]
    }
  ]
}