{
  "info": {
    "name": "Azure Automation API Object Data Types List Fields By Module And Type",
    "_postman_id": "f426361c-1164-40f7-8996-7d7a1b0353ba",
    "description": "Retrieve a list of fields of a given type identified by module name.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "object",
      "item": [
        {
          "id": "aaab5c03-2539-49db-b6d4-8804f53f4a9f",
          "name": "ObjectDataTypes_ListFieldsByModuleAndType",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Automation/automationAccounts/:automationAccountName/modules/:moduleName/objectDataTypes/:typeName/fields"
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
              "id": "5bbd3f5b-cb48-4781-9663-34e582775b84"
            }
          ]
        }
      ]
    }
  ]
}