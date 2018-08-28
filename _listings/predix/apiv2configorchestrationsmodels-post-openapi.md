---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Analytics Runtime Upload a model.
  version: 1.0.0
  description: Upload a model in a multipart MIME structure. The multipart MIME structure
    must have the modelKey  tagged as 'modelKey',  the modelName  tagged as 'modelName',  the
    modelVersion  tagged as 'modelVersion',  the file contents tagged as 'file',  a
    description (under 1024 characters) tagged as 'description'. (See the documentation
    for more information regarding these files.)
host: predix-acs.run.aws-usw02-pr.ice.predix.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
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
      tags:
      - Model
      - By
      - Id
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