swagger: "2.0"
x-collection-name: Predix
x-complete: 1
info:
  title: VIEWS
  version: 1.0.0
host: thetaray-anomaly-service.run.aws-usw02-pr.ice.predix.io
basePath: /v1
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