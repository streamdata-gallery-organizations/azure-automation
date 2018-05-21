---
swagger: "2.0"
x-collection-name: Azure Automation
x-complete: 0
info:
  title: Azure Automation API Job Create
  version: 1.0.0
  description: Create a job of the runbook.
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
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/credentials
  : get:
      summary: Credential List By Automation Account
      description: Retrieve a list of credentials.
      operationId: Credential_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecredentials-get
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
      - Credential
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/compilationjobs/{compilationJobId}
  : put:
      summary: Dsc Compilation Job Create
      description: Creates the Dsc compilation job of the configuration.
      operationId: DscCompilationJob_Create
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecompilationjobscompilationjobid-put
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: compilationJobId
        description: The the DSC configuration Id
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters supplied to the create compilation job operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Compilation
      - Job
      - Create
    get:
      summary: Dsc Compilation Job Get
      description: Retrieve the Dsc configuration compilation job identified by job
        id.
      operationId: DscCompilationJob_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecompilationjobscompilationjobid-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: compilationJobId
        description: The Dsc configuration compilation job id
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Compilation
      - Job
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/compilationjobs
  : get:
      summary: Dsc Compilation Job List By Automation Account
      description: Retrieve a list of dsc compilation jobs.
      operationId: DscCompilationJob_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecompilationjobs-get
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
      - Dsc
      - Compilation
      - Job
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/compilationjobs/{jobId}/streams/{jobStreamId}
  : get:
      summary: Dsc Compilation Job Get Stream
      description: Retrieve the job stream identified by job stream id.
      operationId: DscCompilationJob_GetStream
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamecompilationjobsjobidstreamsjobstreamid-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: jobId
        description: The job id
      - in: path
        name: jobStreamId
        description: The job stream id
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Compilation
      - Job
      - ""
      - Stream
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/configurations/{configurationName}
  : delete:
      summary: Dsc Configuration Delete
      description: Delete the dsc configuration identified by configuration name.
      operationId: DscConfiguration_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconfigurationsconfigurationname-delete
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: configurationName
        description: The configuration name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Configuration
    get:
      summary: Dsc Configuration Get
      description: Retrieve the configuration identified by configuration name.
      operationId: DscConfiguration_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconfigurationsconfigurationname-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: configurationName
        description: The configuration name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Configuration
    put:
      summary: Dsc Configuration Create Or Update
      description: Create the configuration identified by configuration name.
      operationId: DscConfiguration_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconfigurationsconfigurationname-put
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: configurationName
        description: The create or update parameters for configuration
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The create or update parameters for configuration
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Configuration
      - Or
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/configurations/{configurationName}/content
  : get:
      summary: Dsc Configuration Get Content
      description: Retrieve the configuration script identified by configuration name.
      operationId: DscConfiguration_GetContent
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconfigurationsconfigurationnamecontent-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: configurationName
        description: The configuration name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Configuration
      - ""
      - Content
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/configurations
  : get:
      summary: Dsc Configuration List By Automation Account
      description: Retrieve a list of configurations.
      operationId: DscConfiguration_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameconfigurations-get
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
      - Dsc
      - Configuration
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/agentRegistrationInformation
  : get:
      summary: Agent Registration Information Get
      description: Retrieve the automation agent registration information.
      operationId: AgentRegistrationInformation_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameagentregistrationinformation-get
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
      - Agent
      - Registration
      - Information
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/agentRegistrationInformation/regenerateKey
  : post:
      summary: Agent Registration Information Regenerate Key
      description: Regenerate a primary or secondary agent registration key
      operationId: AgentRegistrationInformation_RegenerateKey
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnameagentregistrationinformationregeneratekey-post
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The name of the agent registration key to be regenerated
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Agent
      - Registration
      - Information
      - Regenerate
      - Key
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodes/{nodeId}
  : delete:
      summary: Dsc Node Delete
      description: Delete the dsc node identified by node id.
      operationId: DscNode_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamenodesnodeid-delete
      parameters:
      - in: path
        name: automationAccountName
        description: Automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: The node id
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
    get:
      summary: Dsc Node Get
      description: Retrieve the dsc node identified by node id.
      operationId: DscNode_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamenodesnodeid-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: The node id
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
    patch:
      summary: Dsc Node Update
      description: Update the dsc node.
      operationId: DscNode_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamenodesnodeid-patch
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: Parameters supplied to the update dsc node
      - in: body
        name: parameters
        description: Parameters supplied to the update dsc node
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodes
  : get:
      summary: Dsc Node List By Automation Account
      description: Retrieve a list of dsc nodes.
      operationId: DscNode_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamenodes-get
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
      - Dsc
      - Node
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodes/{nodeId}/reports
  : get:
      summary: Node Reports List By Node
      description: Retrieve the Dsc node report list by node id.
      operationId: NodeReports_ListByNode
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamenodesnodeidreports-get
      parameters:
      - in: query
        name: $filter
        description: The filter to apply on the operation
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: The parameters supplied to the list operation
      responses:
        200:
          description: OK
      tags:
      - Node
      - Reports
      - ListNode
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodes/{nodeId}/reports/{reportId}
  : get:
      summary: Node Reports Get
      description: Retrieve the Dsc node report data by node id and report id.
      operationId: NodeReports_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamenodesnodeidreportsreportid-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: The Dsc node id
      - in: path
        name: reportId
        description: The report id
      responses:
        200:
          description: OK
      tags:
      - Node
      - Reports
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodes/{nodeId}/reports/{reportId}/content
  : get:
      summary: Node Reports Get Content
      description: Retrieve the Dsc node reports by node id and report id.
      operationId: NodeReports_GetContent
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamenodesnodeidreportsreportidcontent-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeId
        description: The Dsc node id
      - in: path
        name: reportId
        description: The report id
      responses:
        200:
          description: OK
      tags:
      - Node
      - Reports
      - ""
      - Content
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodeConfigurations/{nodeConfigurationName}
  : delete:
      summary: Dsc Node Configuration Delete
      description: Delete the Dsc node configurations by node configuration.
      operationId: DscNodeConfiguration_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamenodeconfigurationsnodeconfigurationname-delete
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeConfigurationName
        description: The Dsc node configuration name
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
      - Configuration
    get:
      summary: Dsc Node Configuration Get
      description: Retrieve the Dsc node configurations by node configuration.
      operationId: DscNodeConfiguration_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamenodeconfigurationsnodeconfigurationname-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeConfigurationName
        description: The Dsc node configuration name
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
      - Configuration
    put:
      summary: Dsc Node Configuration Create Or Update
      description: Create the node configuration identified by node configuration
        name.
      operationId: DscNodeConfiguration_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamenodeconfigurationsnodeconfigurationname-put
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: query
        name: No Name
      - in: path
        name: nodeConfigurationName
        description: The create or update parameters for configuration
      - in: body
        name: parameters
        description: The create or update parameters for configuration
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Dsc
      - Node
      - Configuration
      - Or
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/nodeConfigurations
  : get:
      summary: Dsc Node Configuration List By Automation Account
      description: Retrieve a list of dsc node configurations.
      operationId: DscNodeConfiguration_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamenodeconfigurations-get
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
      - Dsc
      - Node
      - Configuration
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/hybridRunbookWorkerGroups/{hybridRunbookWorkerGroupName}
  : delete:
      summary: Hybrid Runbook Worker Group Delete
      description: Delete a hybrid runbook worker group.
      operationId: HybridRunbookWorkerGroup_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamehybridrunbookworkergroupshybridrunbookworkergroupname-delete
      parameters:
      - in: path
        name: automationAccountName
        description: Automation account name
      - in: path
        name: hybridRunbookWorkerGroupName
        description: The hybrid runbook worker group name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Hybrid
      - Runbook
      - Worker
      - Group
    get:
      summary: Hybrid Runbook Worker Group Get
      description: Retrieve a hybrid runbook worker group.
      operationId: HybridRunbookWorkerGroup_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamehybridrunbookworkergroupshybridrunbookworkergroupname-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: hybridRunbookWorkerGroupName
        description: The hybrid runbook worker group name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Hybrid
      - Runbook
      - Worker
      - Group
    patch:
      summary: Hybrid Runbook Worker Group Update
      description: Update a hybrid runbook worker group.
      operationId: HybridRunbookWorkerGroup_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamehybridrunbookworkergroupshybridrunbookworkergroupname-patch
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: hybridRunbookWorkerGroupName
        description: The hybrid runbook worker group name
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The hybrid runbook worker group
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Hybrid
      - Runbook
      - Worker
      - Group
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/hybridRunbookWorkerGroups
  : get:
      summary: Hybrid Runbook Worker Group List By Automation Account
      description: Retrieve a list of hybrid runbook worker groups.
      operationId: HybridRunbookWorkerGroup_ListByAutomationAccount
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamehybridrunbookworkergroups-get
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
      - Hybrid
      - Runbook
      - Worker
      - Group
      - List
      - Automation
      - Account
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/jobs/{jobId}/output
  : get:
      summary: Job Get Output
      description: Retrieve the job output identified by job id.
      operationId: Job_GetOutput
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamejobsjobidoutput-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: jobId
        description: The job id
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Job
      - ""
      - Output
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/jobs/{jobId}/runbookContent
  : get:
      summary: Job Get Runbook Content
      description: Retrieve the runbook content of the job identified by job id.
      operationId: Job_GetRunbookContent
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamejobsjobidrunbookcontent-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: jobId
        description: The job id
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Job
      - ""
      - Runbook
      - Content
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/jobs/{jobId}/suspend
  : post:
      summary: Job Suspend
      description: Suspend the job identified by jobId.
      operationId: Job_Suspend
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamejobsjobidsuspend-post
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: jobId
        description: The job id
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Job
      - Suspend
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/jobs/{jobId}/stop
  : post:
      summary: Job Stop
      description: Stop the job identified by jobId.
      operationId: Job_Stop
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamejobsjobidstop-post
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: jobId
        description: The job id
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Job
      - Stop
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/jobs/{jobId}
  : get:
      summary: Job Get
      description: Retrieve the job identified by job id.
      operationId: Job_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamejobsjobid-get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: jobId
        description: The job id
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Job
    put:
      summary: Job Create
      description: Create a job of the runbook.
      operationId: Job_Create
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftautomationautomationaccountsautomationaccountnamejobsjobid-put
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: jobId
        description: The job id
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters supplied to the create job operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Job
      - Create
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