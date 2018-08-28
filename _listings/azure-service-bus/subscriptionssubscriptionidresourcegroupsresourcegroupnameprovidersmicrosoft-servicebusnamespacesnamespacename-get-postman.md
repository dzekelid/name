{
  "info": {
    "name": "Azure Service Bus API Namespaces Get",
    "_postman_id": "9c1007ca-367c-4adf-8a9d-f9ab8c4b74a0",
    "description": "Gets a description for the specified namespace.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces",
      "item": [
        {
          "id": "289ba1d3-2e57-451b-a6f3-b3b930f69373",
          "name": "Namespaces_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ServiceBus/namespaces/:namespaceName"
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
                },
                {
                  "id": "namespaceName",
                  "value": "namespaceName",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a description for the specified namespace"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "47d117bd-ed14-4f0d-b0ae-d8551f3eb571"
            }
          ]
        }
      ]
    }
  ]
}