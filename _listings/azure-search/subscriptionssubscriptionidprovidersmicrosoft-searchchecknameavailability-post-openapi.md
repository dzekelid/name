---
swagger: "2.0"
x-collection-name: Azure Search
x-complete: 0
info:
  title: Azure Search API Services Check Name Availability
  description: Checks whether or not the given Search service name is available for
    use. Search service names must be globally unique since they are part of the service
    URI (https://<name>.search.windows.net).
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
  /subscriptions/{subscriptionId}/providers/Microsoft.Search/checkNameAvailability:
    post:
      summary: Services Check Name Availability
      description: Checks whether or not the given Search service name is available
        for use. Search service names must be globally unique since they are part
        of the service URI (https://<name>.search.windows.net).
      operationId: Services_CheckNameAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-searchchecknameavailability-post
      parameters:
      - in: body
        name: checkNameAvailabilityInput
        description: The resource name and type to check
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Services Name Availability
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