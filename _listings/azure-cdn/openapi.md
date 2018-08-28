---
swagger: "2.0"
x-collection-name: Azure CDN
x-complete: 1
info:
  title: CdnManagementClient
  description: use-these-apis-to-manage-azure-cdn-resources-through-the-azure-resource-manager--you-must-make-sure-that-requests-made-to-these-resources-are-secure-
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
---