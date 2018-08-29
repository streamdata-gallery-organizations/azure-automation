---
swagger: "2.0"
x-collection-name: Azure Automation
x-complete: 0
info:
  title: Azure Automation API Automation Account Get
  version: 1.0.0
  description: Get information about an Automation Account.
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}
  : patch:
      summary: Automation Account Update
      description: Update an automation account.
      operationId: AutomationAccount_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountname-patch
      parameters:
      - in: path
        name: automationAccountName
        description: Automation account name
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters supplied to the update automation account
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Automation
      - Account
    put:
      summary: Automation Account Create Or Update
      description: Create or update automation account.
      operationId: AutomationAccount_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountname-put
      parameters:
      - in: path
        name: automationAccountName
        description: Parameters supplied to the create or update automation account
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters supplied to the create or update automation account
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Automation
      - Account
      - Or
    delete:
      summary: Automation Account Delete
      description: Delete an automation account.
      operationId: AutomationAccount_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountname-delete
      parameters:
      - in: path
        name: automationAccountName
        description: Automation account name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Automation
      - Account
    get:
      summary: Automation Account Get
      description: Get information about an Automation Account.
      operationId: AutomationAccount_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountname-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Automation
      - Account
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