---
swagger: "2.0"
x-collection-name: AWS OpsWorks
x-complete: 1
info:
  title: AWS OpsWorks API
  version: 1.0.0
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
---