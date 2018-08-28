---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Dynamic Mapping Return locations for an asset by query condition for
    given customer id and collection name.
  description: |-
    Returns the locations for an asset by three types of query for a given customer id and collection name.
    The returned locations are in descending order of time.
    Three types of query:
    1. type=latest: The latest n locations will be returned.
    2. type=timeperiod: Locations within a time period will be returned.
    3. type=bbox: Locations within a time period and a spatial bounding box will be returned.
  version: 1.0.0
host: time-series-service-doc.grc-apps.svc.ice.ge.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/catalog/analytics/versions:
    get:
      summary: Get all versions of the analytic catalog entry with the given name.
      description: Returns all versions of the analytic catalog entry with the given
        name.
      operationId: retrieveByName
      x-api-path-slug: apiv1cataloganalyticsversions-get
      parameters:
      - in: query
        name: name
        description: analytic name
      responses:
        2:
          description: Successful response
      tags:
      - Versions
      - Of
      - Analytic
      - Catalog
      - Entry
      - Given
      - Name
  /api/v2/config/orchestrations/models:
    post:
      summary: Upload a model.
      description: Upload a model in a multipart MIME structure. The multipart MIME
        structure must have the modelKey  tagged as 'modelKey',  the modelName  tagged
        as 'modelName',  the modelVersion  tagged as 'modelVersion',  the file contents
        tagged as 'file',  a description (under 1024 characters) tagged as 'description'.
        (See the documentation for more information regarding these files.)
      operationId: uploadModel
      x-api-path-slug: apiv2configorchestrationsmodels-post
      parameters:
      - in: header
        name: Authorization
        description: Authorization
      - in: formData
        name: description
        description: Artifact description
      - in: formData
        name: file
        description: (Required) Model file
      - in: formData
        name: modelKey
        description: (Required) Model Key
      - in: formData
        name: modelName
        description: (Required) Model Name
      - in: formData
        name: modelVersion
        description: (Required) Model Version
      - in: header
        name: Predix-Zone-Id
        description: Predix-Zone-Id
      responses:
        2:
          description: Successful response
        200:
          description: Successful response
      tags:
      - Upload
      - Model
  /api/v2/config/orchestrations/models/{id}:
    put:
      summary: Update model by id.
      description: Update a model with attributes of the supplied multipart MIME structure.
        The multipart MIME structure must have the modelKey  tagged as 'modelKey',  the
        modelName  tagged as 'modelName',  the modelVersion  tagged as 'modelVersion',  the
        file contents tagged as 'file',  a description (under 1024 characters) tagged
        as 'description'. (See the documentation for more information regarding these
        files.)
      operationId: updateModel
      x-api-path-slug: apiv2configorchestrationsmodelsid-put
      parameters:
      - in: header
        name: Authorization
        description: Authorization
      - in: formData
        name: description
        description: Artifact description
      - in: formData
        name: file
        description: (Required) Model file
      - in: path
        name: id
        description: artifact id
      - in: formData
        name: modelKey
        description: (Required) Model Key
      - in: formData
        name: modelName
        description: (Required) Model Name
      - in: formData
        name: modelVersion
        description: (Required) Model Version
      - in: header
        name: Predix-Zone-Id
        description: Predix-Zone-Id
      responses:
        2:
          description: Successful response
        200:
          description: Successful response
      tags:
      - Model
      - By
      - Id
  /v1/collections/{collectionName}/assets/{assetId}/query:
    post:
      summary: Return locations for an asset by query condition for given customer
        id and collection name.
      description: |-
        Returns the locations for an asset by three types of query for a given customer id and collection name.
        The returned locations are in descending order of time.
        Three types of query:
        1. type=latest: The latest n locations will be returned.
        2. type=timeperiod: Locations within a time period will be returned.
        3. type=bbox: Locations within a time period and a spatial bounding box will be returned.
      operationId: returns-the-locations-for-an-asset-by-three-types-of-query-for-a-given-customer-id-and-collection-na
      x-api-path-slug: v1collectionscollectionnameassetsassetidquery-post
      parameters:
      - in: body
        name: body
        description: The parameters for the query for asset locations
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: Successful response
      tags:
      - Return
      - Locationsan
      - Asset
      - By
      - Query
      - Conditiongiven
      - Customer
      - Id
      - Collection
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