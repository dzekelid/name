---
swagger: "2.0"
x-collection-name: Envestnet
x-complete: 0
info:
  title: Crunch Base Get Organization Relationships
  description: Get Organizations Relationships Using Permlink
  termsOfService: https://data.crunchbase.com/v3/page/accessing-the-dataset
  contact:
    name: Crunchbase
    url: https://groups.google.com/forum/#!forum/crunchbase-api
    email: data@crunchbase.com
  version: v3
host: api.crunchbase.com
basePath: /v/3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /acquisitions/{uuid}/{relationship_name}:
    get:
      summary: Get Acquisitions Relationships
      description: Get Acquisitions Relationships
      operationId: acquisitionsRelationships
      x-api-path-slug: acquisitionsuuidrelationship-name-get
      parameters:
      - in: query
        name: page
        description: The number of the page to retrieve
      - in: path
        name: relationship_name
        description: The name of the relationship connecting Items
      - in: query
        name: sort_order
        description: The sort order
      - in: path
        name: uuid
        description: 32-character uuid of the Acquisition
      responses:
        200:
          description: OK
      tags:
      - Acquisitions
      - Uuid
      - Relationship
      - Name
  /funding-rounds/{uuid}/{relationship_name}:
    get:
      summary: Get Funding Rounds Relationships
      description: Get Funding Rounds Relationships
      operationId: fundingRoundRelationships
      x-api-path-slug: fundingroundsuuidrelationship-name-get
      parameters:
      - in: query
        name: page
        description: The page number to retrieve
      - in: path
        name: relationship_name
        description: The name of the relationship connecting Items
      - in: query
        name: sort_order
        description: The sort order
      - in: path
        name: uuid
        description: The 32-character uuid of the FundingRound
      responses:
        200:
          description: OK
      tags:
      - Funding
      - Rounds
      - Uuid
      - Relationship
      - Name
  /funds/:uuid/{relationship_name}:
    get:
      summary: Get Fund Relationships
      description: Get Fund Relationships
      operationId: fundRelationships
      x-api-path-slug: fundsuuidrelationship-name-get
      parameters:
      - in: query
        name: page
        description: The number of the page to retrieve
      - in: path
        name: relationship_name
        description: The name of the connection between the Fund and related Items
      - in: query
        name: sort_order
        description: The sort order
      - in: path
        name: uuid
        description: The 32-character identifier of the Fund
      responses:
        200:
          description: OK
      tags:
      - Funds
      - :uuid
      - Relationship
      - Name
  /ipos/{uuid}/{relationship_name}:
    get:
      summary: Get IPO Relationships
      description: Get IPO Relationships
      operationId: ipoRelationships
      x-api-path-slug: iposuuidrelationship-name-get
      parameters:
      - in: query
        name: order
        description: The sort order
      - in: path
        name: relationship_name
        description: The name of the relationship connecting Items
      - in: query
        name: The page number to retrieve
        description: The page number to retrieve
      - in: path
        name: uuid
        description: The 32-character identifier of the Ipo
      responses:
        200:
          description: OK
      tags:
      - Ipos
      - Uuid
      - Relationship
      - Name
  /organizations/{permalink}/{relationship_name}:
    get:
      summary: Get Organization Relationships
      description: Get Organizations Relationships Using Permlink
      operationId: organizationRelationships
      x-api-path-slug: organizationspermalinkrelationship-name-get
      parameters:
      - in: query
        name: page
        description: Page number to retrieve
      - in: path
        name: permalink
        description: The permalink of the organization
      - in: path
        name: relationship_name
        description: The name of the rleationship to attached items
      - in: query
        name: sort_order
        description: The sort order
      - in: query
        name: user_key
        description: 'Possible values are: 7a582a92032069b4f775a15b1acbe256'
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Permalink
      - Relationship
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