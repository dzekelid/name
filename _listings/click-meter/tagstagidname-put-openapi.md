---
swagger: "2.0"
x-collection-name: Click Meter
x-complete: 0
info:
  title: Click Meter Fast patch a tag name
  description: Fast patch a tag name.
  contact:
    name: Api Support
    url: http://www.clickmeter.com/api
    email: api@clickmeter.com
  version: v2
host: apiv2.clickmeter.com:80
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tags/{tagId}/name:
    put:
      summary: Fast patch a tag name
      description: Fast patch a tag name.
      operationId: putTagsTagName
      x-api-path-slug: tagstagidname-put
      parameters:
      - in: body
        name: data
        description: The body patch
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: tagId
        description: Id of the tag
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
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