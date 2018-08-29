{
  "info": {
    "name": "Azure Automation API List Operations",
    "_postman_id": "dd0ee6d7-4b21-4569-8649-b39211e16f64",
    "description": "Lists all of the available Automation REST API operations.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "list",
      "item": [
        {
          "id": "e8659fc0-dce5-40e9-bb17-7e4eb41f0700",
          "name": "Operations_List",
          "request": {
            "url": "http://management.azure.com/providers/Microsoft.Automation/operations?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all of the available Automation REST API operations"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "544d3dab-d5f0-43be-89b6-3f569a178229"
            }
          ]
        }
      ]
    }
  ]
}