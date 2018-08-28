---
name: Azure CDN
x-slug: azure-cdn
description: Ensuring a consistent user experience is important. If your websites
  or mobile apps involve streaming media, gaming software, firmware updates (Smart
  TVs, consumer electronic appliances) or IoT endpoints (cars, sensors), Content Delivery
  Network helps you reduce load times, save bandwidth, and increase responsiveness.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/02-delivery.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-cdn/apis.md
specificationVersion: "0.14"
apis:
- name: Azure CDN API Check Name Availability
  x-api-slug: azure-cdn-api
  description: Check the availability of a resource name. This is needed for resources
    where name is globally unique, such as a CDN endpoint.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/02-delivery.png
  humanURL: https://azure.microsoft.com/en-us/services/cdn/
  baseURL: ://management.azure.com////providers/Microsoft.Cdn/checkNameAvailability
  tags: CDN,Name Availability
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-cdn/providersmicrosoft-cdnchecknameavailability-post-openapi.md
- name: Azure CDN API
  x-api-slug: azure-cdn-api
  description: Ensuring a consistent user experience is important. If your websites
    or mobile apps involve streaming media, gaming software, firmware updates (Smart
    TVs, consumer electronic appliances) or IoT endpoints (cars, sensors), Content
    Delivery Network helps you reduce load times, save bandwidth, and increase responsiveness.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/02-delivery.png
  humanURL: https://azure.microsoft.com/en-us/services/cdn/
  baseURL: ://management.azure.com//
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-cdn/openapi.md
x-common:
- type: x-documentation
  url: https://docs.microsoft.com/en-us/azure/cdn/
- type: x-pricing
  url: https://azure.microsoft.com/en-us/pricing/details/cdn/
- type: x-website
  url: https://azure.microsoft.com/en-us/services/cdn/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---