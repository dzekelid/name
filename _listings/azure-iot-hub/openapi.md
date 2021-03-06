---
swagger: "2.0"
x-collection-name: Azure IoT Hub
x-complete: 1
info:
  title: iotHubClient
  description: use-this-api-to-manage-the-iot-hubs-in-your-subscription-
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
  /subscriptions/{subscriptionId}/providers/Microsoft.Devices/checkNameAvailability:
    post:
      summary: Iot Hub Resource Check Name Availability
      description: Check if an IoT hub name is available.
      operationId: IotHubResource_CheckNameAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-deviceschecknameavailability-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: operationInputs
        description: Set the name parameter in the OperationInputs structure to the
          name of the IoT hub to check
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Iot Hub Resource Name Availability
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Devices/IotHubs/{resourceName}/IotHubKeys/{keyName}/listkeys
  : post:
      summary: Iot Hub Resource Get Keys For Key Name
      description: 'Get a shared access policy by name from an IoT hub. For more information,
        see: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-security.'
      operationId: IotHubResource_GetKeysForKeyName
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-devicesiothubsresourcenameiothubkeyskeynamelistkeys-post
      parameters:
      - in: path
        name: keyName
        description: The name of the shared access policy
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group that contains the IoT hub
      - in: path
        name: resourceName
        description: The name of the IoT hub
      responses:
        200:
          description: OK
      tags:
      - Iot Hub Resource Keys For Key Name
---