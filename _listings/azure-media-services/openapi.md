---
swagger: "2.0"
x-collection-name: Azure Media Services
x-complete: 1
info:
  title: MediaServicesManagementClient
  description: media-services-resource-management-apis-
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
  /subscriptions/{subscriptionId}/providers/Microsoft.Media/CheckNameAvailability:
    post:
      summary: Media Service Check Name Availability
      description: Checks whether the Media Service resource name is available. The
        name must be globally unique.
      operationId: MediaService_CheckNameAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-mediachecknameavailability-post
      parameters:
      - in: body
        name: CheckNameAvailabilityInput
        description: Properties needed to check the availability of a name
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Media Service Name Availability
---