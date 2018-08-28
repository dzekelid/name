---
swagger: "2.0"
x-collection-name: AWS Machine Learning
x-complete: 0
info:
  title: AWS Machine Learning API Update Evaluation
  version: 1.0.0
  description: Updates the EvaluationName of an Evaluation.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=UpdateBatchPrediction:
    get:
      summary: Update Batch Prediction
      description: Updates the BatchPredictionName of a BatchPrediction.
      operationId: updateBatchPrediction
      x-api-path-slug: actionupdatebatchprediction-get
      parameters:
      - in: query
        name: BatchPredictionId
        description: The ID assigned to the BatchPrediction during creation
        type: string
      - in: query
        name: BatchPredictionName
        description: A new user-supplied name or description of the BatchPrediction
        type: string
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Batches
  /?Action=UpdateDataSource:
    get:
      summary: Update Data Source
      description: Updates the DataSourceName of a DataSource.
      operationId: updateDataSource
      x-api-path-slug: actionupdatedatasource-get
      parameters:
      - in: query
        name: DataSourceId
        description: The ID assigned to the DataSource during creation
        type: string
      - in: query
        name: DataSourceName
        description: A new user-supplied name or description of the DataSource that
          will replace the current description
        type: string
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Data Sources
  /?Action=UpdateEvaluation:
    get:
      summary: Update Evaluation
      description: Updates the EvaluationName of an Evaluation.
      operationId: updateEvaluation
      x-api-path-slug: actionupdateevaluation-get
      parameters:
      - in: query
        name: EvaluationId
        description: The ID assigned to the Evaluation during creation
        type: string
      - in: query
        name: EvaluationName
        description: A new user-supplied name or description of the Evaluation that
          will replace the current content
        type: string
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Evaluations
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