{
  "info": {
    "name": "Azure Notification Hubs API Namespaces Get",
    "_postman_id": "8f892396-752b-4f63-bb68-c14a3ae4ed8c",
    "description": "Returns the description for the specified namespace.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces",
      "item": [
        {
          "id": "5cac72d2-ceb9-4a54-8df4-42692e314a23",
          "name": "Namespaces_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.NotificationHubs/namespaces/:namespaceName"
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
                  "id": "namespaceName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "resourceGroupName",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the description for the specified namespace"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6c5bb138-8875-49b9-b2b7-5887438e53da"
            }
          ]
        }
      ]
    }
  ]
}