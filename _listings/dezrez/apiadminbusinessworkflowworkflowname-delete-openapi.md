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