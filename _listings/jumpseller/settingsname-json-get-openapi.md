---
swagger: "2.0"
x-collection-name: Jumpseller
x-complete: 0
info:
  title: Jumpseller Get Settings Name
  description: ""
  version: "1"
host: api.jumpseller.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /settings/{name}.json:
    get:
      summary: Get Settings Name
      description: ""
      operationId: getSettingsName.json
      x-api-path-slug: settingsname-json-get
      parameters:
      - in: path
        name: name
        description: Name of the Store Setting
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Settings
      - Name
      - Json
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