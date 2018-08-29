{
  "info": {
    "name": "Azure Automation API Test Job Streams Get",
    "_postman_id": "a380d984-dc5e-4038-99d7-11920a080fea",
    "description": "Retrieve a test job streams identified by runbook name and stream id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "test",
      "item": [
        {
          "id": "5f6e03dc-3cdc-46d8-a4ea-b406a538cb0c",
          "name": "TestJobStreams_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/runbooks/:runbookName/draft/testJob/streams/:jobStreamId"
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
                  "id": "jobStreamId",
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
            "description": "Retrieve a test job streams identified by runbook name and stream id"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0c03a2e-2d20-47e8-ad49-ad8fac86763f"
            }
          ]
        }
      ]
    }
  ]
}