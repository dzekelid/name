---
swagger: "2.0"
x-collection-name: Steem
x-complete: 0
info:
  title: Steem get_api_by_name
  description: get_api_by_name
  version: 1.0.0
host: api.steemjs.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /get_api_by_name:
    get:
      summary: get_api_by_name
      description: get_api_by_name
      operationId: get-api-by-name
      x-api-path-slug: get-api-by-name-get
      parameters:
      - in: query
        name: apiName
        description: apiName
      responses:
        200:
          description: OK
      tags:
      - Get
      - Api
      - By
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