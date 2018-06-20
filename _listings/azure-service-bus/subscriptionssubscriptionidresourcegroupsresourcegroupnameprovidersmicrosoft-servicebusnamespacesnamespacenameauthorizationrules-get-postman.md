{
  "info": {
    "name": "Azure Service Bus API Namespaces List Authorization Rules",
    "_postman_id": "44e604fe-7ede-417d-835d-e536b9c73338",
    "description": "Gets the authorization rules for a namespace.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces authorization rules",
      "item": [
        {
          "id": "3b4c8119-b52e-41fd-adad-3cda872e38e9",
          "name": "Namespaces_ListAuthorizationRules",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ServiceBus/namespaces/:namespaceName/AuthorizationRules"
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
            "description": "Gets the authorization rules for a namespace"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9865a4be-c32b-429b-9bc7-2f025b02cda8"
            }
          ]
        }
      ]
    }
  ]
}