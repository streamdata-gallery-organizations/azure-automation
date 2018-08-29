{
  "info": {
    "name": "Azure Automation API Credential List By Automation Account",
    "_postman_id": "ee69b6b7-e729-4b5e-8f5b-0130040f8b7c",
    "description": "Retrieve a list of credentials.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "credential",
      "item": [
        {
          "id": "c223b770-3eec-4567-bcce-8880cd340fc3",
          "name": "Credential_ListByAutomationAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/credentials"
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
            "description": "Retrieve a list of credentials"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cde3e212-0c12-43ad-a038-75c2b93f7f72"
            }
          ]
        }
      ]
    }
  ]
}