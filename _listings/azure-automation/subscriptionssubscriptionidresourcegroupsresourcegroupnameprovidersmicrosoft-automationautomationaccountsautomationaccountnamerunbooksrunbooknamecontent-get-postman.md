{
  "info": {
    "name": "Azure Automation API Runbook Get Content",
    "_postman_id": "fb567d9f-cf42-4c79-b4fc-b22d1210f538",
    "description": "Retrieve the content of runbook identified by runbook name.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "runbook",
      "item": [
        {
          "id": "5836d439-ca81-4363-8366-8ccee320f407",
          "name": "Runbook_GetContent",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/runbooks/:runbookName/content"
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
                  "id": "runbookName",
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
            "description": "Retrieve the content of runbook identified by runbook name"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6e187d55-1a93-4eeb-9437-19f9d5d7f98e"
            }
          ]
        }
      ]
    }
  ]
}