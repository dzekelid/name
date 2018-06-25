---
name: Azure DocumentDB
x-slug: azure-documentdb
description: Azure DocumentDB is a fully-managed NoSQL document database service that
  offers querying and transaction-processing over schema-free data, predictable and
  reliable performance, and rapid development.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-document-db-03-replicate.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-documentdb/apis.md
specificationVersion: "0.14"
apis:
- name: Azure DocumentDB API Database Accounts Check Name Exists
  x-api-slug: azure-documentdb-api
  description: Checks that the Azure DocumentDB account name already exists. A valid
    account name may contain only lowercase letters, numbers, and the '-' character,
    and must be between 3 and 50 characters.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-document-db-03-replicate.png
  humanURL: https://azure.microsoft.com/en-us/services/documentdb/
  baseURL: ://management.azure.com////providers/Microsoft.DocumentDB/databaseAccountNames/{accountName}
  tags: Database, Accounts, Checks, Name, Exists
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-documentdb/providersmicrosoft-documentdbdatabaseaccountnamesaccountname-head-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-documentdb/providersmicrosoft-documentdbdatabaseaccountnamesaccountname-head-openapi.md
- name: Azure DocumentDB API
  x-api-slug: azure-documentdb-api
  description: Azure DocumentDB is a fully-managed NoSQL document database service
    that offers querying and transaction-processing over schema-free data, predictable
    and reliable performance, and rapid development.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-document-db-03-replicate.png
  humanURL: https://azure.microsoft.com/en-us/services/documentdb/
  baseURL: ://management.azure.com//
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-documentdb/openapi.md
x-common:
- type: x-documentation
  url: https://docs.microsoft.com/en-us/azure/documentdb/
- type: x-pricing
  url: https://azure.microsoft.com/en-us/pricing/details/documentdb/
- type: x-service-level-agreements
  url: https://azure.microsoft.com/en-us/support/legal/sla/documentdb/
- type: x-status
  url: https://azure.microsoft.com/en-us/status/
- type: x-website
  url: https://azure.microsoft.com/en-us/services/documentdb/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---