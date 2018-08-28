---
swagger: "2.0"
x-collection-name: AWS OpsWorks
x-complete: 0
info:
  title: AWS OpsWorks API Get Hostname Suggestion
  version: 1.0.0
  description: Gets a generated host name for the specified layer, based on the current
    host name theme.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=GetHostnameSuggestion:
    get:
      summary: Get Hostname Suggestion
      description: Gets a generated host name for the specified layer, based on the
        current host name theme.
      operationId: getHostnameSuggestion
      x-api-path-slug: actiongethostnamesuggestion-get
      parameters:
      - in: query
        name: LayerId
        description: The layer ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Hostname
      - Suggestion
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