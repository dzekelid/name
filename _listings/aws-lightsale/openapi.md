---
swagger: "2.0"
x-collection-name: AWS Lightsale
x-complete: 1
info:
  title: AWS Lightsale API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=GetActiveNames:
    get:
      summary: Get Active Names
      description: Returns the names of all active (not deleted) resources.
      operationId: getActiveNames
      x-api-path-slug: actiongetactivenames-get
      parameters:
      - in: query
        name: pageToken
        description: A token used for paginating results from your get active names
          request
        type: string
      responses:
        200:
          description: OK
      tags:
      - Names
---