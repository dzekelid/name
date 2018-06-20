{
  "info": {
    "name": "Azure Event Hubs API Namespaces List By Subscription",
    "_postman_id": "3c17a1e5-5577-4240-aede-6b2189468d8e",
    "description": "Lists all the available Namespaces within a subscription, irrespective of the resource groups.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces subscription",
      "item": [
        {
          "id": "0e86434a-fc1e-4adc-9d2b-b8629bdbc393",
          "name": "Namespaces_ListBySubscription",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.EventHub/namespaces"
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
            "description": "Lists all the available Namespaces within a subscription, irrespective of the resource groups"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "faf9fad6-c687-4b50-9b28-d8bfcf611326"
            }
          ]
        }
      ]
    }
  ]
}