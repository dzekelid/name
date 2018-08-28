---
swagger: "2.0"
x-collection-name: Azure Storage
x-complete: 1
info:
  title: StorSimpleSeries8000ManagementClient
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
  /subscriptions/{subscriptionId}/providers/Microsoft.Storage/checkNameAvailability:
    post:
      summary: Storage Accounts Check Name Availability
      description: Checks that the storage account name is valid and is not already
        in use.
      operationId: StorageAccounts_CheckNameAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-storagechecknameavailability-post
      parameters:
      - in: body
        name: accountName
        description: The name of the storage account within the specified resource
          group
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts Name Availability
---