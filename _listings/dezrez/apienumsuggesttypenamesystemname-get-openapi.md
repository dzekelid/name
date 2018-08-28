---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Get enum suggestions for value
  version: 1.0.0
  description: Get enum suggestions for value.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
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
        2:
          description: Successful response
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