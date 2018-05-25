{
  "info": {
    "name": "Azure Automation API Object Data Types List Fields By Type",
    "_postman_id": "777e5324-cc00-49e9-9800-4fe7a2193fe0",
    "description": "Retrieve a list of fields of a given type across all accessible modules.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "object",
      "item": [
        {
          "id": "ad85a7a2-748e-409e-9a37-317aedf46b19",
          "name": "ObjectDataTypes_ListFieldsByType",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/objectDataTypes/:typeName/fields"
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
                  "id": "typeName",
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
            "description": "Retrieve a list of fields of a given type across all accessible modules"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b50537c4-a674-4aa2-aaf7-9f2a79dd6e10"
            }
          ]
        }
      ]
    }
  ]
}