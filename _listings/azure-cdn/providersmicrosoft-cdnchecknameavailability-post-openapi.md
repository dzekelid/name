---
swagger: "2.0"
x-collection-name: Azure CDN
x-complete: 0
info:
  title: Azure CDN API Check Name Availability
  description: Check the availability of a resource name. This is needed for resources
    where name is globally unique, such as a CDN endpoint.
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /providers/Microsoft.Cdn/checkNameAvailability:
    post:
      summary: Check Name Availability
      description: Check the availability of a resource name. This is needed for resources
        where name is globally unique, such as a CDN endpoint.
      operationId: CheckNameAvailability
      x-api-path-slug: providersmicrosoft-cdnchecknameavailability-post
      parameters:
      - in: body
        name: checkNameAvailabilityInput
        description: Input to check
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - CDN
      - Name Availability
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