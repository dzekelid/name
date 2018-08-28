---
swagger: "2.0"
x-collection-name: Azure Notification Hubs
x-complete: 1
info:
  title: NotificationHubsManagementClient
  description: azure-notificationhub-client
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
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NotificationHubs/namespaces/{namespaceName}
  : put:
      summary: Namespaces Create Or Update
      description: Creates/Updates a service namespace. Once created, this namespace's
        resource manifest is immutable. This operation is idempotent.
      operationId: Namespaces_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacename-put
      parameters:
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters supplied to create a Namespace Resource
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces
    patch:
      summary: Namespaces Patch
      description: Patches the existing namespace
      operationId: Namespaces_Patch
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacename-patch
      parameters:
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters supplied to patch a Namespace Resource
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces
    delete:
      summary: Namespaces Delete
      description: Deletes an existing namespace. This operation also removes all
        associated notificationHubs under the namespace.
      operationId: Namespaces_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacename-delete
      parameters:
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces
    get:
      summary: Namespaces Get
      description: Returns the description for the specified namespace.
      operationId: Namespaces_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacename-get
      parameters:
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NotificationHubs/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}
  : put:
      summary: Namespaces Create Or Update Authorization Rule
      description: Creates an authorization rule for a namespace
      operationId: Namespaces_CreateOrUpdateAuthorizationRule
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacenameauthorizationrulesauthorizationrulename-put
      parameters:
      - in: path
        name: authorizationRuleName
        description: Aauthorization Rule Name
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The shared access authorization rule
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rule
    delete:
      summary: Namespaces Delete Authorization Rule
      description: Deletes a namespace authorization rule
      operationId: Namespaces_DeleteAuthorizationRule
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacenameauthorizationrulesauthorizationrulename-delete
      parameters:
      - in: path
        name: authorizationRuleName
        description: Authorization Rule Name
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rule
    get:
      summary: Namespaces Get Authorization Rule
      description: Gets an authorization rule for a namespace by name.
      operationId: Namespaces_GetAuthorizationRule
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacenameauthorizationrulesauthorizationrulename-get
      parameters:
      - in: path
        name: authorizationRuleName
        description: Authorization rule name
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rule
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NotificationHubs/namespaces:
    get:
      summary: Namespaces List
      description: Lists the available namespaces within a resourceGroup.
      operationId: Namespaces_List
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespaces-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces
  /subscriptions/{subscriptionId}/providers/Microsoft.NotificationHubs/namespaces:
    get:
      summary: Namespaces List All
      description: Lists all the available namespaces within the subscription irrespective
        of the resourceGroups.
      operationId: Namespaces_ListAll
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-notificationhubsnamespaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces All
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NotificationHubs/namespaces/{namespaceName}/AuthorizationRules
  : get:
      summary: Namespaces List Authorization Rules
      description: Gets the authorization rules for a namespace.
      operationId: Namespaces_ListAuthorizationRules
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacenameauthorizationrules-get
      parameters:
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rules
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NotificationHubs/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}/listKeys
  : post:
      summary: Namespaces List Keys
      description: Gets the Primary and Secondary ConnectionStrings to the namespace
      operationId: Namespaces_ListKeys
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacenameauthorizationrulesauthorizationrulenamelistkeys-post
      parameters:
      - in: path
        name: authorizationRuleName
        description: The connection string of the namespace for the specified authorizationRule
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces Keys
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.NotificationHubs/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}/regenerateKeys
  : post:
      summary: Namespaces Regenerate Keys
      description: Regenerates the Primary/Secondary Keys to the Namespace Authorization
        Rule
      operationId: Namespaces_RegenerateKeys
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-notificationhubsnamespacesnamespacenameauthorizationrulesauthorizationrulenameregeneratekeys-post
      parameters:
      - in: path
        name: authorizationRuleName
        description: The connection string of the namespace for the specified authorizationRule
      - in: path
        name: namespaceName
        description: The namespace name
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters supplied to regenerate the Namespace Authorization
          Rule Key
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Namespaces Regenerate Keys
---