---
swagger: "2.0"
x-collection-name: Broadleaf Commerce
x-complete: 0
info:
  title: Broadleaf Commerce API Post Loggers Name
  description: Post loggers name.
  version: 1.0.0
host: demo.broadleafcommerce.org
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /env/{name}:
    get:
      summary: Get Env Name
      description: Get env name.
      operationId: getEnvName
      x-api-path-slug: envname-get
      parameters:
      - in: path
        name: name
        description: name
      responses:
        200:
          description: OK
      tags:
      - Env
      - Name
  /loggers/{name}:
    get:
      summary: Get Loggers Name
      description: Get loggers name.
      operationId: getLoggersName
      x-api-path-slug: loggersname-get
      parameters:
      - in: path
        name: name
        description: name
      responses:
        200:
          description: OK
      tags:
      - Loggers
      - Name
    post:
      summary: Post Loggers Name
      description: Post loggers name.
      operationId: postLoggersName
      x-api-path-slug: loggersname-post
      parameters:
      - in: body
        name: configuration
        description: configuration
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: name
      responses:
        200:
          description: OK
      tags:
      - Loggers
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