{
  "info": {
    "name": "Azure Automation API Test Job Streams List By Test Job",
    "_postman_id": "83da7f1a-34ad-47c1-98e3-59a69d9edef9",
    "description": "Retrieve a list of test job streams identified by runbook name.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "test",
      "item": [
        {
          "id": "38602aea-a77b-4ad5-86fb-5356b69fe7f4",
          "name": "TestJobStreams_ListByTestJob",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/runbooks/:runbookName/draft/testJob/streams"
              ],
              "query": [
                {
                  "key": "$filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
            "description": "Retrieve a list of test job streams identified by runbook name"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8063c47f-284c-4f85-baac-c2af849c3081"
            }
          ]
        }
      ]
    }
  ]
}