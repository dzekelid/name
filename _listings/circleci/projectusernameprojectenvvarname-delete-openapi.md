---
swagger: "2.0"
x-collection-name: CircleCI
x-complete: 0
info:
  title: CircleCI Delete Project Username Project Envvar Name
  description: Deletes the environment variable named ':name'
  version: 1.0.0
host: circleci.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /project/{username}/{project}/envvar/{name}:
    delete:
      summary: Delete Project Username Project Envvar Name
      description: Deletes the environment variable named ':name'
      operationId: deleteProjectUsernameProjectEnvvarName
      x-api-path-slug: projectusernameprojectenvvarname-delete
      responses:
        200:
          description: OK
      tags:
      - Project
      - Username
      - Project
      - Envvar
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