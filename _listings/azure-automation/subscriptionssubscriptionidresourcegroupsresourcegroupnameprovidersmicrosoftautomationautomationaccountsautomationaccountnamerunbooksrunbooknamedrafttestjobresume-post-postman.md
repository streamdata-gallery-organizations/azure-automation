{
  "info": {
    "name": "Azure Automation API Test Jobs Resume",
    "_postman_id": "5bcc626d-aa4f-4bc3-abe5-c6e0a555781a",
    "description": "Resume the test job.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "test",
      "item": [
        {
          "id": "ba6b871e-b254-4314-b54d-9b047791bbf4",
          "name": "TestJobs_Resume",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/runbooks/:runbookName/draft/testJob/resume"
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
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Resume the test job"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "440495af-0ecc-45f0-b422-2963f522179c"
            }
          ]
        }
      ]
    }
  ]
}