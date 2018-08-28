{
  "info": {
    "name": "Azure Service Bus API Namespaces List By Subscription",
    "_postman_id": "66adca6b-5db3-44ad-9d9d-1202d2580c51",
    "description": "Gets all the available namespaces within the subscription, irrespective of the resource groups.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces subscription",
      "item": [
        {
          "id": "236f2619-be54-4233-b2d3-5a8a6c81ed70",
          "name": "Namespaces_ListBySubscription",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.ServiceBus/namespaces"
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
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets all the available namespaces within the subscription, irrespective of the resource groups"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f66c3125-e7f1-4449-9fbc-1abf292b6fbc"
            }
          ]
        }
      ]
    }
  ]
}