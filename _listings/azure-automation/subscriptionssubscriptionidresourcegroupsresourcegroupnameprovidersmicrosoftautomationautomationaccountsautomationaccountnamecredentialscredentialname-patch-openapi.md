---
swagger: "2.0"
x-collection-name: Azure Automation
x-complete: 0
info:
  title: Azure Automation API Credential Update
  version: 1.0.0
  description: Update a credential.
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
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts:
    get:
      summary: Automation Account List By Resource Group
      description: Retrieve a list of accounts within a given resource group.
      operationId: AutomationAccount_ListByResourceGroup
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccounts-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Automation
      - Account
      - List
      - Resource
      - Group
  /providers/Microsoft.Automation/operations:
    get:
      summary: List Operations
      description: Lists all of the available Automation REST API operations.
      operationId: Operations_List
      x-api-path-slug: providersmicrosoftautomationoperations-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - List
      - Operations
  /subscriptions/{subscriptionId}/providers/Microsoft.Automation/automationAccounts:
    get:
      summary: Lists the Automation Accounts
      description: Retrieve a list of accounts within a given subscription.
      operationId: AutomationAccount_List
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoftautomationautomationaccounts-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Lists
      - Automation
      - Accounts
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/statistics
  : get:
      summary: Statistics List By Automation Account
      description: Retrieve the statistics for the account.
      operationId: Statistics_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamestatistics-get
      parameters:
      - in: query
        name: $filter
        description: The filter to apply on the operation
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Statistics
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/usages
  : get:
      summary: Usages List By Automation Account
      description: Retrieve the usage for the account id.
      operationId: Usages_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameusages-get
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
      - Usages
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/certificates/{certificateName}
  : delete:
      summary: Certificate Delete
      description: Delete the certificate.
      operationId: Certificate_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecertificatescertificatename-delete
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: certificateName
        description: The name of certificate
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Certificate
    get:
      summary: Certificate Get
      description: Retrieve the certificate identified by certificate name.
      operationId: Certificate_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecertificatescertificatename-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: certificateName
        description: The name of certificate
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Certificate
    put:
      summary: Certificate Create Or Update
      description: Create a certificate.
      operationId: Certificate_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecertificatescertificatename-put
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: certificateName
        description: The parameters supplied to the create or update certificate operation
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters supplied to the create or update certificate operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Certificate
      - Or
    patch:
      summary: Certificate Update
      description: Update a certificate.
      operationId: Certificate_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecertificatescertificatename-patch
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: certificateName
        description: The parameters supplied to the update certificate operation
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters supplied to the update certificate operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Certificate
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/certificates
  : get:
      summary: Certificate List By Automation Account
      description: Retrieve a list of certificates.
      operationId: Certificate_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecertificates-get
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
      - Certificate
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/connections/{connectionName}
  : delete:
      summary: Connection Delete
      description: Delete the connection.
      operationId: Connection_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconnectionsconnectionname-delete
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: connectionName
        description: The name of connection
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Connection
    get:
      summary: Connection Get
      description: Retrieve the connection identified by connection name.
      operationId: Connection_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconnectionsconnectionname-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: connectionName
        description: The name of connection
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Connection
    put:
      summary: Connection Create Or Update
      description: Create or update a connection.
      operationId: Connection_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconnectionsconnectionname-put
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
      - Connection
      - Or
    patch:
      summary: Connection Update
      description: Update a connection.
      operationId: Connection_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconnectionsconnectionname-patch
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: connectionName
        description: The parameters supplied to the update a connection operation
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters supplied to the update a connection operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Connection
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/connections
  : get:
      summary: Connection List By Automation Account
      description: Retrieve a list of connections.
      operationId: Connection_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconnections-get
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
      - Connection
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/connectionTypes/{connectionTypeName}
  : delete:
      summary: Connection Type Delete
      description: Delete the connectiontype.
      operationId: ConnectionType_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconnectiontypesconnectiontypename-delete
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: connectionTypeName
        description: The name of connectiontype
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Connection
      - Type
    get:
      summary: Connection Type Get
      description: Retrieve the connectiontype identified by connectiontype name.
      operationId: ConnectionType_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconnectiontypesconnectiontypename-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: connectionTypeName
        description: The name of connectiontype
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Connection
      - Type
    put:
      summary: Connection Type Create Or Update
      description: Create a connectiontype.
      operationId: ConnectionType_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconnectiontypesconnectiontypename-put
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: connectionTypeName
        description: The parameters supplied to the create or update connectiontype
          operation
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters supplied to the create or update connectiontype
          operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Connection
      - Type
      - Or
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/connectionTypes
  : get:
      summary: Connection Type List By Automation Account
      description: Retrieve a list of connectiontypes.
      operationId: ConnectionType_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconnectiontypes-get
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
      - Connection
      - Type
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/credentials/{credentialName}
  : delete:
      summary: Credential Delete
      description: Delete the credential.
      operationId: Credential_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecredentialscredentialname-delete
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: credentialName
        description: The name of credential
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Credential
    get:
      summary: Credential Get
      description: Retrieve the credential identified by credential name.
      operationId: Credential_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecredentialscredentialname-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: credentialName
        description: The name of credential
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Credential
    put:
      summary: Credential Create Or Update
      description: Create a credential.
      operationId: Credential_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecredentialscredentialname-put
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: credentialName
        description: The parameters supplied to the create or update credential operation
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters supplied to the create or update credential operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Credential
      - Or
    patch:
      summary: Credential Update
      description: Update a credential.
      operationId: Credential_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecredentialscredentialname-patch
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: credentialName
        description: The parameters supplied to the Update credential operation
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters supplied to the Update credential operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Credential
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