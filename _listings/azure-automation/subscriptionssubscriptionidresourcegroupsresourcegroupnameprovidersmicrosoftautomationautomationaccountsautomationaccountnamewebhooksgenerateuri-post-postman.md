{
  "info": {
    "name": "Azure Automation API Webhook Generate Uri",
    "_postman_id": "c8d27b91-d618-42f0-9a8c-8166a9fab29f",
    "description": "Generates a Uri for use in creating a webhook.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "webhook",
      "item": [
        {
          "id": "ebe7c846-151a-4bde-8f95-ca689d3cfcf9",
          "name": "Webhook_GenerateUri",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/webhooks/generateUri"
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
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Generates a Uri for use in creating a webhook"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e59adf85-1fcf-4be7-a97e-fb8e97755e42"
            }
          ]
        }
      ]
    }
  ]
}