---
swagger: "2.0"
x-collection-name: Azure Traffic Manager
x-complete: 1
info:
  title: TrafficManagerManagementClient
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
  /providers/Microsoft.Network/checkTrafficManagerNameAvailability:
    post:
      summary: Profiles Check Traffic Manager Relative Dns Name Availability
      description: Checks the availability of a Traffic Manager Relative DNS name.
      operationId: Profiles_CheckTrafficManagerRelativeDnsNameAvailability
      x-api-path-slug: providersmicrosoft-networkchecktrafficmanagernameavailability-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The Traffic Manager name parameters supplied to the CheckTrafficManagerNameAvailability
          operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Profiles Traffic Manager Relative Dns Name Availability
---