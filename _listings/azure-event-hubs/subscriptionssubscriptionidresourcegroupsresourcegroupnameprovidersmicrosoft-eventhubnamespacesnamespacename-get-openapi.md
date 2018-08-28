---
swagger: "2.0"
x-collection-name: Azure Event Hubs
x-complete: 0
info:
  title: Azure Event Hubs API Namespaces Get
  description: Gets the description of the specified namespace.
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
  /subscriptions/{subscriptionId}/providers/Microsoft.EventHub/namespaces:
    get:
      summary: Namespaces List By Subscription
      description: Lists all the available Namespaces within a subscription, irrespective
        of the resource groups.
      operationId: Namespaces_ListBySubscription
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-eventhubnamespaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Subscription
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces:
    get:
      summary: Namespaces List By Resource Group
      description: Lists the available Namespaces within a resource group.
      operationId: Namespaces_ListByResourceGroup
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Resource Group
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}:
    put:
      summary: Namespaces Create Or Update
      description: Creates or updates a namespace. Once created, this namespace's
        resource manifest is immutable. This operation is idempotent.
      operationId: Namespaces_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters for creating a namespace resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces
    delete:
      summary: Namespaces Delete
      description: Deletes an existing namespace. This operation also removes all
        associated resources under the namespace.
      operationId: Namespaces_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces
    get:
      summary: Namespaces Get
      description: Gets the description of the specified namespace.
      operationId: Namespaces_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces
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