---
swagger: "2.0"
x-collection-name: Dyn
x-complete: 1
info:
  title: Dyn
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  xheaders:
    get:
      summary: Retrieving a list of custom X-header field names
      description: Retrieving a list of custom X-header field names
      operationId: getXheaders
      x-api-path-slug: xheaders-get
      parameters:
      - in: query
        name: apikey
        description: Required
      responses:
        200:
          description: OK
      tags:
      - Retrievinglist
      - of
      - custom
      - X-header
      - field
      - names
---