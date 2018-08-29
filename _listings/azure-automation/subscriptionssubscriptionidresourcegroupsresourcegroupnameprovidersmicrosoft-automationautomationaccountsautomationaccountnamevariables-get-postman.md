{
  "info": {
    "name": "Azure Automation API Variable List By Automation Account",
    "_postman_id": "b8228598-ca7c-4c38-a1cb-49c66380a244",
    "description": "Retrieve a list of variables.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "variable",
      "item": [
        {
          "id": "5816d8d2-cd29-4192-97d9-96705512f5f9",
          "name": "Variable_ListByAutomationAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/variables"
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
            "description": "Retrieve a list of variables"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "482633ec-abe2-44c2-91d4-90fcc8ae62b1"
            }
          ]
        }
      ]
    }
  ]
}