{
  "info": {
    "name": "Azure Event Hubs API Namespaces List Authorization Rules",
    "_postman_id": "701ca78d-0c02-4aa5-973f-1fd08d3686bb",
    "description": "Gets a list of authorization rules for a Namespace.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces authorization rules",
      "item": [
        {
          "id": "7e7a6bab-f2dd-496e-83bc-cb56355d20cf",
          "name": "Namespaces_ListAuthorizationRules",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.EventHub/namespaces/:namespaceName/AuthorizationRules"
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
            "description": "Gets a list of authorization rules for a Namespace"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d8ae37d3-b133-4a71-b192-cbea5c8c35dd"
            }
          ]
        }
      ]
    }
  ]
}