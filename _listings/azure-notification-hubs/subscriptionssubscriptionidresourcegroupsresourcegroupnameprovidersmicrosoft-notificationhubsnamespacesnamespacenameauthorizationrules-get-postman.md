{
  "info": {
    "name": "Azure Notification Hubs API Namespaces List Authorization Rules",
    "_postman_id": "15cb092e-0c99-46f4-ba6e-9eb36435ee8d",
    "description": "Gets the authorization rules for a namespace.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces authorization rules",
      "item": [
        {
          "id": "82a5027b-f47b-4b36-935d-0c00ac23c23c",
          "name": "Namespaces_ListAuthorizationRules",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.NotificationHubs/namespaces/:namespaceName/AuthorizationRules"
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
            "description": "Gets the authorization rules for a namespace"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "71de4c81-fbfe-4345-9a41-b3476ce168dc"
            }
          ]
        }
      ]
    }
  ]
}