{
  "info": {
    "name": "Azure IoT Hub API Iot Hub Resource Get Keys For Key Name",
    "_postman_id": "e7c5a5dc-783b-422b-b76b-a97f2ba29be9",
    "description": "Get a shared access policy by name from an IoT hub. For more information, see: https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-security.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "iot hub resource keys for key name",
      "item": [
        {
          "id": "93ca636b-468d-4b4c-a3bf-f9aa0143ff0d",
          "name": "IotHubResource_GetKeysForKeyName",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Devices/IotHubs/:resourceName/IotHubKeys/:keyName/listkeys"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "keyName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "resourceGroupName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "resourceName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Get a shared access policy by name from an IoT hub"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7f30b5aa-bd8a-4d23-bbaf-b583eb55ecd9"
            }
          ]
        }
      ]
    }
  ]
}