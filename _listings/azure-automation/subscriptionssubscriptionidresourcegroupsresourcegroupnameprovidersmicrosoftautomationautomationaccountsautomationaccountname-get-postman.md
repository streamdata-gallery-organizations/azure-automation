{
  "info": {
    "name": "Azure Automation API Automation Account Get",
    "_postman_id": "5b4dc519-ecb8-425f-8aaa-c55ada62913a",
    "description": "Get information about an Automation Account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "automation",
      "item": [
        {
          "id": "c3cfb3e7-0f5f-40d4-b459-3b157ff5b357",
          "name": "AutomationAccount_Get",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get information about an Automation Account"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ea2de569-ac08-49a6-97bb-dd3c8dd2eda7"
            }
          ]
        }
      ]
    }
  ]
}