---
swagger: "2.0"
x-collection-name: Azure Search
x-complete: 1
info:
  title: SearchManagementClient
  description: client-that-can-be-used-to-manage-azure-search-services-and-api-keys-
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
---