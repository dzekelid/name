---
name: Azure IoT Hub
x-slug: azure-iot-hub
description: Jumpstart your Internet of Things project with Microsoft IoT Hub. Connect,
  monitor, and control billions of IoT assets running on a broad set of operating
  systems and protocols. Establish reliable, bi-directional communication with these
  assets, even if they&rsquo;re intermittently connected, and analyze&mdash;and act
  on&mdash;incoming telemetry data. Enhance the security of your IoT solutions by
  using per-device authentication to communicate with devices that have the appropriate
  credentials. Revoke access rights to specific devices to maintain the integrity
  of your system.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-iot-01-establish.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-iot-hub/apis.md
specificationVersion: "0.14"
apis:
- name: Azure IoT Hub API Iot Hub Resource Check Name Availability
  x-api-slug: azure-iot-hub-api
  description: Check if an IoT hub name is available.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-iot-01-establish.png
  humanURL: https://azure.microsoft.com/en-us/services/iot-hub/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/providers/Microsoft.Devices/checkNameAvailability
  tags: Iot Hub Resource Name Availability
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-iot-hub/subscriptionssubscriptionidprovidersmicrosoft-deviceschecknameavailability-post-openapi.md
- name: Azure IoT Hub API Iot Hub Resource Get Keys For Key Name
  x-api-slug: azure-iot-hub-api
  description: 'Get a shared access policy by name from an IoT hub. For more information,
    see: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-security.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-iot-01-establish.png
  humanURL: https://azure.microsoft.com/en-us/services/iot-hub/
  baseURL: ://management.azure.com////subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Devices/IotHubs/{resourceName}/IotHubKeys/{keyName}/listkeys
  tags: Iot Hub Resource Keys For Key Name
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-iot-hub/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devicesiothubsresourcenameiothubkeyskeynamelistkeys-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-iot-hub/subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devicesiothubsresourcenameiothubkeyskeynamelistkeys-post-openapi.md
- name: Azure IoT Hub API
  x-api-slug: azure-iot-hub-api
  description: Jumpstart your Internet of Things project with Microsoft IoT Hub. Connect,
    monitor, and control billions of IoT assets running on a broad set of operating
    systems and protocols. Establish reliable, bi-directional communication with these
    assets, even if they&rsquo;re intermittently connected, and analyze&mdash;and
    act on&mdash;incoming telemetry data. Enhance the security of your IoT solutions
    by using per-device authentication to communicate with devices that have the appropriate
    credentials. Revoke access rights to specific devices to maintain the integrity
    of your system.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-iot-01-establish.png
  humanURL: https://azure.microsoft.com/en-us/services/iot-hub/
  baseURL: ://management.azure.com//
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/azure-iot-hub/openapi.md
x-common:
- type: x-documentation
  url: https://docs.microsoft.com/en-us/azure/iot-hub/
- type: x-pricing
  url: https://azure.microsoft.com/en-us/pricing/details/iot-hub/
- type: x-service-level-agreements
  url: https://azure.microsoft.com/en-us/support/legal/sla/iot-hub/
- type: x-status
  url: https://azure.microsoft.com/en-us/status/
- type: x-website
  url: https://azure.microsoft.com/en-us/services/iot-hub/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---