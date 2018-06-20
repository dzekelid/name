---
swagger: "2.0"
x-collection-name: AWS API Gateway
x-complete: 0
info:
  title: AWS API Gateway API Model Byname
  version: 1.0.0
  description: Gets information about the Model of a specified name.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /domainnames/mon-api.com:
    delete:
      summary: Domainname Delete
      description: Deletes the domain name resource.
      operationId: domainnameDelete
      x-api-path-slug: domainnamesmonapi-com-delete
      parameters:
      - in: header
        name: Authorization
        type: string
      - in: header
        name: Content-Type
        type: string
      - in: header
        name: Host
        type: string
      - in: header
        name: X-Amz-Date
        type: string
      responses:
        200:
          description: OK
      tags:
      - Domainname
  /restapis/uojnr9hd57/models/output:
    get:
      summary: Model Byname
      description: Gets information about the Model of a specified name.
      operationId: modelBy-name
      x-api-path-slug: restapisuojnr9hd57modelsoutput-get
      parameters:
      - in: header
        name: Authorization
        type: string
      - in: header
        name: Content-Type
        type: string
      - in: header
        name: Host
        type: string
      - in: header
        name: X-Amz-Date
        type: string
      responses:
        200:
          description: OK
      tags:
      - Model
      - Byname
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