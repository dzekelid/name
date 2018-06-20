{
  "info": {
    "name": "Azure Service Bus API Namespaces List By Resource Group",
    "_postman_id": "a951561a-a930-48e2-8838-cbbcc99b9f4f",
    "description": "Gets the available namespaces within a resource group.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces resource group",
      "item": [
        {
          "id": "2a1c8ca3-8065-43f9-b73c-eddf8d9fddc9",
          "name": "Namespaces_ListByResourceGroup",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ServiceBus/namespaces"
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
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                },
                {
                  "id": "resourceGroupName",
                  "value": "resourceGroupName",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the available namespaces within a resource group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "81ecd09e-7759-4bd1-a4e7-4ac7382380c6"
            }
          ]
        }
      ]
    }
  ]
}