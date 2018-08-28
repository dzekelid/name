---
swagger: "2.0"
x-collection-name: Azure Service Bus
x-complete: 0
info:
  title: Azure Service Bus API Namespaces List Keys
  description: Gets the primary and secondary connection strings for the namespace.
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
  /subscriptions/{subscriptionId}/providers/Microsoft.ServiceBus/CheckNameAvailability:
    post:
      summary: Namespaces Check Name Availability
      description: Check the give namespace name availability.
      operationId: Namespaces_CheckNameAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-servicebuschecknameavailability-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters to check availability of the given namespace name
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces Name Availability
  /subscriptions/{subscriptionId}/providers/Microsoft.ServiceBus/namespaces:
    get:
      summary: Namespaces List By Subscription
      description: Gets all the available namespaces within the subscription, irrespective
        of the resource groups.
      operationId: Namespaces_ListBySubscription
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-servicebusnamespaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Subscription
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ServiceBus/namespaces:
    get:
      summary: Namespaces List By Resource Group
      description: Gets the available namespaces within a resource group.
      operationId: Namespaces_ListByResourceGroup
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-servicebusnamespaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Resource Group
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ServiceBus/namespaces/{namespaceName}:
    put:
      summary: Namespaces Create Or Update
      description: Creates or updates a service namespace. Once created, this namespace's
        resource manifest is immutable. This operation is idempotent.
      operationId: Namespaces_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-servicebusnamespacesnamespacename-put
      parameters:
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters supplied to create a namespace resource
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
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-servicebusnamespacesnamespacename-delete
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
      description: Gets a description for the specified namespace.
      operationId: Namespaces_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-servicebusnamespacesnamespacename-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces
    patch:
      summary: Namespaces Update
      description: Updates a service namespace. Once created, this namespace's resource
        manifest is immutable. This operation is idempotent.
      operationId: Namespaces_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-servicebusnamespacesnamespacename-patch
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters supplied to update a namespace resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ServiceBus/namespaces/{namespaceName}/AuthorizationRules
  : get:
      summary: Namespaces List Authorization Rules
      description: Gets the authorization rules for a namespace.
      operationId: Namespaces_ListAuthorizationRules
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-servicebusnamespacesnamespacenameauthorizationrules-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rules
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ServiceBus/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}
  : put:
      summary: Namespaces Create Or Update Authorization Rule
      description: Creates or updates an authorization rule for a namespace.
      operationId: Namespaces_CreateOrUpdateAuthorizationRule
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-servicebusnamespacesnamespacenameauthorizationrulesauthorizationrulename-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The shared access authorization rule
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rule
    delete:
      summary: Namespaces Delete Authorization Rule
      description: Deletes a namespace authorization rule.
      operationId: Namespaces_DeleteAuthorizationRule
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-servicebusnamespacesnamespacenameauthorizationrulesauthorizationrulename-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rule
    get:
      summary: Namespaces Get Authorization Rule
      description: Gets an authorization rule for a namespace by rule name.
      operationId: Namespaces_GetAuthorizationRule
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-servicebusnamespacesnamespacenameauthorizationrulesauthorizationrulename-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rule
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ServiceBus/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}/listKeys
  : post:
      summary: Namespaces List Keys
      description: Gets the primary and secondary connection strings for the namespace.
      operationId: Namespaces_ListKeys
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-servicebusnamespacesnamespacenameauthorizationrulesauthorizationrulenamelistkeys-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Keys
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