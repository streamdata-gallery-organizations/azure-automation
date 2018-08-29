{
  "info": {
    "name": "Azure Automation API Dsc Configuration Get Content",
    "_postman_id": "bd413896-8351-461e-b092-3312dafac4fc",
    "description": "Retrieve the configuration script identified by configuration name.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "dsc",
      "item": [
        {
          "id": "97cd3e7c-0ce1-4def-ae58-da1f6afce1f0",
          "name": "DscConfiguration_GetContent",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/configurations/:configurationName/content"
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
                  "id": "configurationName",
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
            "description": "Retrieve the configuration script identified by configuration name"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6a301a99-0550-45bd-ae5a-e899b1fcc456"
            }
          ]
        }
      ]
    }
  ]
}