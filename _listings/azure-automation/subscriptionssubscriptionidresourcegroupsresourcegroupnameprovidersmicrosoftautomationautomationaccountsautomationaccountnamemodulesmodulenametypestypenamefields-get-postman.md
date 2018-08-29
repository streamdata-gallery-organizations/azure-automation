{
  "info": {
    "name": "Azure Automation API Fields List By Type",
    "_postman_id": "ab1b55aa-eff6-4fdd-9253-799f483a5e68",
    "description": "Retrieve a list of fields of a given type identified by module name.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "fields",
      "item": [
        {
          "id": "803efbf8-57ab-4ada-9282-e26bbef591b4",
          "name": "Fields_ListByType",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/modules/:moduleName/types/:typeName/fields"
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
                  "id": "moduleName",
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
            "description": "Retrieve a list of fields of a given type identified by module name"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f9b1bb74-b999-4c78-b7cb-836f14533ee9"
            }
          ]
        }
      ]
    }
  ]
}