---
swagger: "2.0"
x-collection-name: Azure IoT Hub
x-complete: 0
info:
  title: Azure IoT Hub API Iot Hub Resource Check Name Availability
  description: Check if an IoT hub name is available.
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
  /subscriptions/{subscriptionId}/providers/Microsoft.Devices/checkNameAvailability:
    post:
      summary: Iot Hub Resource Check Name Availability
      description: Check if an IoT hub name is available.
      operationId: IotHubResource_CheckNameAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-deviceschecknameavailability-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: operationInputs
        description: Set the name parameter in the OperationInputs structure to the
          name of the IoT hub to check
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Iot Hub Resource Name Availability
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