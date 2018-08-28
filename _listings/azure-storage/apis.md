---
name: Azure Storage
x-slug: azure-storage
description: Azure Storage offers non-relational data storage including Blob Storage,
  Table Storage, Queue Storage, and Files.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-storage.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-storage/apis.md
specificationVersion: "0.14"
apis:
- name: Azure Storage API Storage Accounts Check Name Availability
  x-api-slug: azure-storage-api
  description: Checks that the storage account name is valid and is not already in
    use.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-storage.png
  humanURL: https://azure.microsoft.com/en-us/services/storage/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/providers/Microsoft.Storage/checkNameAvailability
  tags: Storage Accounts Name Availability
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-storage/subscriptionssubscriptionidprovidersmicrosoft-storagechecknameavailability-post-openapi.md
- name: Azure Storage API
  x-api-slug: azure-storage-api
  description: Azure Storage offers non-relational data storage including Blob Storage,
    Table Storage, Queue Storage, and Files.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-storage.png
  humanURL: https://azure.microsoft.com/en-us/services/storage/
  baseURL: ://management.azure.com//
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-storage/openapi.md
x-common:
- type: x-documentation
  url: https://docs.microsoft.com/en-us/azure/storage/
- type: x-pricing
  url: https://azure.microsoft.com/en-us/pricing/details/storage/
- type: x-service-level-agreements
  url: https://azure.microsoft.com/en-us/support/legal/sla/storage/
- type: x-status
  url: https://azure.microsoft.com/en-us/status/
- type: x-website
  url: https://azure.microsoft.com/en-us/services/storage/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---