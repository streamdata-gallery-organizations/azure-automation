{
  "info": {
    "name": "Azure Automation API Job Schedule List By Automation Account",
    "_postman_id": "82d96698-3e29-4bda-a2aa-3ea3d331832f",
    "description": "Retrieve a list of job schedules.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "job",
      "item": [
        {
          "id": "0b214483-a321-427a-b2c4-9302bb9fe646",
          "name": "JobSchedule_ListByAutomationAccount",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/jobSchedules"
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
            "description": "Retrieve a list of job schedules"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "184ef10b-e05d-46c3-b7e7-5a0cf120db42"
            }
          ]
        }
      ]
    }
  ]
}