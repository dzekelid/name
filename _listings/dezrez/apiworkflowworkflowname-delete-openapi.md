---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Terminates a running workflow instance.
  version: 1.0.0
  description: Terminates a running workflow instance..
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/customfieldgroup/{typeName}:
    get:
      summary: Get a list of custom field groups for a type and optional group name
        specified.
      description: Get a list of custom field groups for a type and optional group
        name specified..
      operationId: CustomFieldGroup_GetBytypeNameBygroupName
      x-api-path-slug: apicustomfieldgrouptypename-get
      parameters:
      - in: query
        name: groupName
        description: An optional parameter to filter by group name
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: typeName
        description: The name of the type to get the custom field groups for
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Custom
      - Field
      - Groupsa
      - Type
      - Optional
      - Group
      - Name
      - Specified
  /api/documentgeneration/targetgroups:
    get:
      summary: Get an enum by its type and system name
      description: Get an enum by its type and system name.
      operationId: DocumentGeneration_TargetGroups
      x-api-path-slug: apidocumentgenerationtargetgroups-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Enum
      - By
      - Its
      - Type
      - System
      - Name
  /api/enum/marketingrolestatus:
    get:
      summary: Get an enum by its type and system name
      description: Get an enum by its type and system name.
      operationId: Enum_GetMarketingRoleStatusBytransactionType
      x-api-path-slug: apienummarketingrolestatus-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: transactionType
        description: The typeo of marketingrole to get
      responses:
        200:
          description: OK
      tags:
      - Enum
      - By
      - Its
      - Type
      - System
      - Name
  /api/feature/{name}:
    get:
      summary: Get a feature by its name
      description: Get a feature by its name.
      operationId: Feature_GetByname
      x-api-path-slug: apifeaturename-get
      parameters:
      - in: path
        name: name
        description: The name of the feature to get
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Feature
      - By
      - Its
      - Name
  /api/admin/system/ListAgencies:
    get:
      summary: Lists the name and ID of all agencies in the system.
      description: Lists the name and id of all agencies in the system..
      operationId: System_ListAgenciesByincludeSuspended
      x-api-path-slug: apiadminsystemlistagencies-get
      parameters:
      - in: query
        name: includeSuspended
        description: if set to true [include suspended]
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Lists
      - Name
      - ID
      - Of
      - ""
      - Agencies
      - In
      - System
  /api/tag/{name}:
    get:
      summary: Get a tag by its name
      description: Get a tag by its name.
      operationId: Tag_GetByname
      x-api-path-slug: apitagname-get
      parameters:
      - in: path
        name: name
        description: The name of the tag to get
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Tag
      - By
      - Its
      - Name
  /api/twitter/directmessage:
    post:
      summary: Sends a direct message to a screen name
      description: Sends a direct message to a screen name.
      operationId: Twitter_TwitterDirectMessageBydirectMessage
      x-api-path-slug: apitwitterdirectmessage-post
      parameters:
      - in: body
        name: directMessage
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Sends
      - Direct
      - Message
      - To
      - Screen
      - Name
  /api/twitter/tweet:
    post:
      summary: Sends a direct message to a screen name
      description: Sends a direct message to a screen name.
      operationId: Twitter_TwitterDirectMessageBytweet
      x-api-path-slug: apitwittertweet-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: tweet
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Sends
      - Direct
      - Message
      - To
      - Screen
      - Name
  /api/admin/businessworkflow/{workflowName}:
    get:
      summary: Lists instances of a given workflow
      description: Lists instances of a given workflow.
      operationId: BusinessWorkflow_ListWorkflowInstancesByworkflowNameByskipBytake
      x-api-path-slug: apiadminbusinessworkflowworkflowname-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: skip
      - in: query
        name: take
      - in: path
        name: workflowName
      responses:
        200:
          description: OK
      tags:
      - Lists
      - Instances
      - Of
      - Given
      - Workflow
    delete:
      summary: Terminates a running workflow instance.
      description: Terminates a running workflow instance..
      operationId: BusinessWorkflow_TerminateWorkflowInstanceByworkflowNameByworkflowInstanceHandleByreason
      x-api-path-slug: apiadminbusinessworkflowworkflowname-delete
      parameters:
      - in: query
        name: reason
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: workflowInstanceHandle
      - in: path
        name: workflowName
      responses:
        200:
          description: OK
      tags:
      - Terminates
      - Running
      - Workflow
      - Instance
  /api/documentgeneration/envelopetemplatepacks/{systemName}:
    get:
      summary: Gets a list of the packs for a particular packtype
      description: Gets a list of the packs for a particular packtype.
      operationId: DocumentGeneration_GetEnvelopeTemplatePackForTypeBysystemName
      x-api-path-slug: apidocumentgenerationenvelopetemplatepackssystemname-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: systemName
      responses:
        200:
          description: OK
      tags:
      - S
      - List
      - Of
      - Packsa
      - Particular
      - Packtype
  /api/documentgeneration/envelopetemplatepacksummarys/{systemName}:
    get:
      summary: Gets a list of the packs for a particular packtype
      description: Gets a list of the packs for a particular packtype.
      operationId: DocumentGeneration_GetEnvelopeTemplatePackSummarysForTypeBysystemName
      x-api-path-slug: apidocumentgenerationenvelopetemplatepacksummaryssystemname-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: systemName
      responses:
        200:
          description: OK
      tags:
      - S
      - List
      - Of
      - Packsa
      - Particular
      - Packtype
  /api/enum:
    get:
      summary: "Returns a list of possible values for an enum if you just specify
        {typeName}.\r\nReturns a an enum if you specify {typeName} and {systemName}."
      description: "Returns a list of possible values for an enum if you just specify
        {typename}.\r\nreturns a an enum if you specify {typename} and {systemname}.."
      operationId: Enum_GetBytypeNameBysystemNameByeventCategoryType
      x-api-path-slug: apienum-get
      parameters:
      - in: query
        name: eventCategoryType
        description: Where the enum has values which are categorised, this filters
          on that category
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: systemName
        description: The system name of the enum to get
      - in: query
        name: typeName
        description: The type of enum to get
      responses:
        200:
          description: OK
      tags:
      - Returns
      - List
      - Of
      - Possible
      - Valuesan
      - Enum
      - If
      - You
      - Just
      - Specify
      - TypeName
      - Returns
      - Enum
      - If
      - You
      - Specify
      - TypeName
      - SystemName
  /api/enum/suggest/{typeName}/{systemName}:
    get:
      summary: Get enum suggestions for value
      description: Get enum suggestions for value.
      operationId: Enum_SuggestBytypeNameBysystemName
      x-api-path-slug: apienumsuggesttypenamesystemname-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: systemName
        description: The value to retrieve suggestions for
      - in: path
        name: typeName
        description: The type of enum to get
      responses:
        200:
          description: OK
      tags:
      - Enum
      - Suggestionsvalue
  /api/legacy/{typeName}/{id}:
    get:
      summary: ""
      description: .
      operationId: Legacy_GetByidBytypeName
      x-api-path-slug: apilegacytypenameid-get
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: typeName
      responses:
        200:
          description: OK
      tags:
      - ""
  /api/list/listsearchschema:
    get:
      summary: <param name="filterName">Filter for follow ups</param>
      description: <param name="filtername">filter for follow ups</param>.
      operationId: List_GetListSearchSchemaByfilterName
      x-api-path-slug: apilistlistsearchschema-get
      parameters:
      - in: query
        name: filterName
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - <param
      - Name=filterName>Filterfollow
      - Ups<
      - Param>
  /api/webhook/create/{triggerName}:
    post:
      summary: Creates a new webhook in the system (scoped to agency)
      description: Creates a new webhook in the system (scoped to agency).
      operationId: Webhook_CreateWebhookBytriggerNameBycreateWebhookRequest
      x-api-path-slug: apiwebhookcreatetriggername-post
      parameters:
      - in: body
        name: createWebhookRequest
        description: Webhook callback details
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: triggerName
        description: Name of the trigger
      responses:
        200:
          description: OK
      tags:
      - Creates
      - New
      - Webhook
      - In
      - System
      - (scoped
      - To
      - Agency)
  /api/workflow/{workflowName}:
    get:
      summary: Lists instances of a given workflow
      description: Lists instances of a given workflow.
      operationId: Workflow_ListWorkflowInstancesByworkflowNameByskipBytake
      x-api-path-slug: apiworkflowworkflowname-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: skip
      - in: query
        name: take
      - in: path
        name: workflowName
      responses:
        200:
          description: OK
      tags:
      - Lists
      - Instances
      - Of
      - Given
      - Workflow
    delete:
      summary: Terminates a running workflow instance.
      description: Terminates a running workflow instance..
      operationId: Workflow_TerminateWorkflowInstanceByworkflowNameByworkflowInstanceHandleByreason
      x-api-path-slug: apiworkflowworkflowname-delete
      parameters:
      - in: query
        name: reason
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: workflowInstanceHandle
      - in: path
        name: workflowName
      responses:
        200:
          description: OK
      tags:
      - Terminates
      - Running
      - Workflow
      - Instance
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