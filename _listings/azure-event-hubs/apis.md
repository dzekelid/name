---
name: Azure Event Hubs
x-slug: azure-event-hubs
description: Azure Event Hubs is a hyper-scale telemetry ingestion service that collects,
  transforms, and stores millions of events. As a distributed streaming platform,
  it gives you low latency and configurable time retention, which enables you to ingress
  massive amounts of telemetry into the cloud and read the data from multiple applications
  using publish-subscribe semantics.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/apis.md
specificationVersion: "0.14"
apis:
- name: Azure Event Hubs API Namespaces Check Name Availability
  x-api-slug: azure-event-hubs-api
  description: Check the give Namespace name availability.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/providers/Microsoft.EventHub/CheckNameAvailability
  tags: Namespaces Name Availability
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidprovidersmicrosoft-eventhubchecknameavailability-post-openapi.md
- name: Azure Event Hubs API Namespaces List By Subscription
  x-api-slug: azure-event-hubs-api
  description: Lists all the available Namespaces within a subscription, irrespective
    of the resource groups.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/providers/Microsoft.EventHub/namespaces
  tags: Namespaces Subscription
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidprovidersmicrosoft-eventhubnamespaces-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidprovidersmicrosoft-eventhubnamespaces-get-openapi.md
- name: Azure Event Hubs API Namespaces List By Resource Group
  x-api-slug: azure-event-hubs-api
  description: Lists the available Namespaces within a resource group.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces
  tags: Namespaces Resource Group
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespaces-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespaces-get-openapi.md
- name: Azure Event Hubs API Namespaces Create Or Update
  x-api-slug: azure-event-hubs-api
  description: Creates or updates a namespace. Once created, this namespace's resource
    manifest is immutable. This operation is idempotent.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}
  tags: Namespaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-put-openapi.md
- name: Azure Event Hubs API Namespaces Delete
  x-api-slug: azure-event-hubs-api
  description: Deletes an existing namespace. This operation also removes all associated
    resources under the namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}
  tags: Namespaces
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-delete-openapi.md
- name: Azure Event Hubs API Namespaces Get
  x-api-slug: azure-event-hubs-api
  description: Gets the description of the specified namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}
  tags: Namespaces
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-get-openapi.md
- name: Azure Event Hubs API Namespaces Update
  x-api-slug: azure-event-hubs-api
  description: Creates or updates a namespace. Once created, this namespace's resource
    manifest is immutable. This operation is idempotent.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}
  tags: Namespaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-patch-openapi.md
- name: Azure Event Hubs API Namespaces List Authorization Rules
  x-api-slug: azure-event-hubs-api
  description: Gets a list of authorization rules for a Namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}/AuthorizationRules
  tags: Namespaces Authorization Rules
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrules-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrules-get-openapi.md
- name: Azure Event Hubs API Namespaces Create Or Update Authorization Rule
  x-api-slug: azure-event-hubs-api
  description: Creates or updates an AuthorizationRule for a Namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}
  tags: Namespaces Authorization Rule
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulename-put-openapi.md
- name: Azure Event Hubs API Namespaces Delete Authorization Rule
  x-api-slug: azure-event-hubs-api
  description: Deletes an AuthorizationRule for a Namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}
  tags: Namespaces Authorization Rule
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulename-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulename-delete-openapi.md
- name: Azure Event Hubs API Namespaces Get Authorization Rule
  x-api-slug: azure-event-hubs-api
  description: Gets an AuthorizationRule for a Namespace by rule name.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}
  tags: Namespaces Authorization Rule
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulename-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulename-get-openapi.md
- name: Azure Event Hubs API Namespaces List Keys
  x-api-slug: azure-event-hubs-api
  description: Gets the primary and secondary connection strings for the Namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}/listKeys
  tags: Namespaces Keys
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulenamelistkeys-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulenamelistkeys-post-openapi.md
- name: Azure Event Hubs API Namespaces Regenerate Keys
  x-api-slug: azure-event-hubs-api
  description: Regenerates the primary or secondary connection strings for the specified
    Namespace.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}/regenerateKeys
  tags: Namespaces Regenerate Keys
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulenameregeneratekeys-post-openapi.md
- name: Azure Event Hubs API
  x-api-slug: azure-event-hubs-api
  description: Azure Event Hubs is a hyper-scale telemetry ingestion service that
    collects, transforms, and stores millions of events. As a distributed streaming
    platform, it gives you low latency and configurable time retention, which enables
    you to ingress massive amounts of telemetry into the cloud and read the data from
    multiple applications using publish-subscribe semantics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-event-hubs-stream.png
  humanURL: https://azure.microsoft.com/en-us/services/event-hubs/
  baseURL: ://management.azure.com//
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-event-hubs/openapi.md
x-common:
- type: x-documentation
  url: https://docs.microsoft.com/en-us/azure/event-hubs/
- type: x-pricing
  url: https://azure.microsoft.com/en-us/pricing/details/event-hubs/
- type: x-service-level-agreements
  url: https://azure.microsoft.com/en-us/support/legal/sla/event-hubs/
- type: x-status
  url: https://azure.microsoft.com/en-us/status/
- type: x-website
  url: https://azure.microsoft.com/en-us/services/event-hubs/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---