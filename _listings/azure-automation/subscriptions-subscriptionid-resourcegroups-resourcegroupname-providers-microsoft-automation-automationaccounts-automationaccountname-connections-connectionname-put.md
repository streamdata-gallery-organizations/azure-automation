---
swagger: "2.0"
info:
  title: AutomationManagementClient
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/connections/{connectionName}
  : put:
      summary: Connection Create Or Update
      description: Create or update a connection
      operationId: Connection_CreateOrUpdate
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: connectionName
        description: The parameters supplied to the create or update connection operation
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters supplied to the create or update connection operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - connection
      - or
definitions:
  ActivityParameter:
    properties: []
x-collection-name: Azure Automation
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---