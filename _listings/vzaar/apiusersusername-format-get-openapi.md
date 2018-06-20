---
swagger: "2.0"
x-collection-name: Vzaar
x-complete: 0
info:
  title: Vzaar API Get Api Users Username
  description: nnThis API call returns the users public details along with its relevant
    metadata.nn
  termsOfService: http://vzaar.com/policies
  version: v1
host: vzaar.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/users/{username}.{format}:
    get:
      summary: Get Api Users Username
      description: nnThis API call returns the users public details along with its
        relevant metadata.nn
      operationId: getApiUsersUsername.Format
      x-api-path-slug: apiusersusername-format-get
      parameters:
      - in: query
        name: 'username is the vzaar login name for the user. Note: This must be the
          actual username and not the email address'
      responses:
        200:
          description: OK
      tags:
      - Api
      - Users
      - Username
      - Format
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