{
  "info": {
    "name": "Azure Automation API Job List By Automation Account",
    "_postman_id": "4b084b28-edbd-4d95-8924-1af6aee3f457",
    "description": "Retrieve a list of jobs.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "job",
      "item": [
        {
          "id": "7d72f92d-e1a0-4f84-8979-0f036fff54ca",
          "name": "Job_ListByAutomationAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/jobs"
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
            "description": "Retrieve a list of jobs"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d5917674-80ad-4aa2-af58-b436b27cfb85"
            }
          ]
        }
      ]
    }
  ]
}