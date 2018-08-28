swagger: "2.0"
x-collection-name: AWS Machine Learning
x-complete: 1
info:
  title: AWS Machine Learning API
  version: 1.0.0
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
  /?Action=UpdateMLModel:
    get:
      summary: Update M L Model
      description: Updates the MLModelName and the ScoreThreshold of an MLModel.
      operationId: updateMLModel
      x-api-path-slug: actionupdatemlmodel-get
      parameters:
      - in: query
        name: MLModelId
        description: The ID assigned to the MLModel during creation
        type: string
      - in: query
        name: MLModelName
        description: A user-supplied name or description of the MLModel
        type: string
      - in: query
        name: ScoreThreshold
        description: The ScoreThreshold used in binary classification MLModel that
          marks the boundary between a positive prediction and a negative prediction
        type: string
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Models