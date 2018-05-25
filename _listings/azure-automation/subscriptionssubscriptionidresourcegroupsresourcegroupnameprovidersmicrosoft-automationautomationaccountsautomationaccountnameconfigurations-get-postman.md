{
  "info": {
    "name": "Azure Automation API Dsc Configuration List By Automation Account",
    "_postman_id": "e95eae1c-5ada-47ed-b008-a5b9e4de15b6",
    "description": "Retrieve a list of configurations.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "dsc",
      "item": [
        {
          "id": "ddc93ba1-97f5-485b-834b-f163cbb896cd",
          "name": "DscConfiguration_ListByAutomationAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/configurations"
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
            "description": "Retrieve a list of configurations"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b63c9666-b409-4a75-9953-e1eaa6d53a8f"
            }
          ]
        }
      ]
    }
  ]
}