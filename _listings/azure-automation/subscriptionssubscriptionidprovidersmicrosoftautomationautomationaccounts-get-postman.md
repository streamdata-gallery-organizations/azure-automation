{
  "info": {
    "name": "Azure Automation API Lists the Automation Accounts",
    "_postman_id": "09f5e271-f62e-4c63-b992-682e760b4f0c",
    "description": "Retrieve a list of accounts within a given subscription.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "lists",
      "item": [
        {
          "id": "4f282a52-fd92-454b-9614-4615c574dd5f",
          "name": "AutomationAccount_List",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.Automation/automationAccounts"
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
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a list of accounts within a given subscription"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b8cd617e-adbe-4b20-bd17-b2bad7470ec7"
            }
          ]
        }
      ]
    }
  ]
}