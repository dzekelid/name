---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Sends a direct message to a screen name
  version: 1.0.0
  description: Sends a direct message to a screen name.
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