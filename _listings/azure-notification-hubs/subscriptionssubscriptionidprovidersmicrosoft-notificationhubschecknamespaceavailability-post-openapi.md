---
swagger: "2.0"
x-collection-name: Azure Notification Hubs
x-complete: 0
info:
  title: Azure Notification Hubs API Namespaces Check Availability
  description: Checks the availability of the given service namespace across all Azure
    subscriptions. This is useful because the domain name is created based on the
    service namespace name.
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
  /subscriptions/{subscriptionId}/providers/Microsoft.NotificationHubs/checkNamespaceAvailability:
    post:
      summary: Namespaces Check Availability
      description: Checks the availability of the given service namespace across all
        Azure subscriptions. This is useful because the domain name is created based
        on the service namespace name.
      operationId: Namespaces_CheckAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-notificationhubschecknamespaceavailability-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The namespace name
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces Availability
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