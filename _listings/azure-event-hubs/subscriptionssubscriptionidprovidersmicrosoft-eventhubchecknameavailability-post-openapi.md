---
swagger: "2.0"
x-collection-name: Azure Event Hubs
x-complete: 0
info:
  title: Azure Event Hubs API Namespaces Check Name Availability
  description: Check the give Namespace name availability.
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
  /subscriptions/{subscriptionId}/providers/Microsoft.EventHub/CheckNameAvailability:
    post:
      summary: Namespaces Check Name Availability
      description: Check the give Namespace name availability.
      operationId: Namespaces_CheckNameAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-eventhubchecknameavailability-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters to check availability of the given Namespace name
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces Name Availability
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