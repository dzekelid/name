---
swagger: "2.0"
x-collection-name: Envestnet
x-complete: 0
info:
  title: Crunch Base Get Fund Relationships
  description: Get Fund Relationships
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