---
swagger: "2.0"
x-collection-name: AWS API Gateway
x-complete: 1
info:
  title: AWS API Gateway API
  version: 1.0.0
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
---