---
swagger: "2.0"
x-collection-name: Dyn
x-complete: 0
info:
  title: Dyn Retrieving a list of custom X-header field names
  version: 1.0.0
  description: Retrieving a list of custom X-header field names
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