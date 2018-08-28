{
  "info": {
    "name": "Azure Event Hubs API Namespaces List Keys",
    "_postman_id": "c71738ff-7e13-4c42-ac62-25ed4ac5cfaf",
    "description": "Gets the primary and secondary connection strings for the Namespace.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces keys",
      "item": [
        {
          "id": "79b2be4b-916f-46b5-a4e9-41e0b3ad6883",
          "name": "Namespaces_ListKeys",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.EventHub/namespaces/:namespaceName/AuthorizationRules/:authorizationRuleName/listKeys"
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
                },
                {
                  "id": "authorizationRuleName",
                  "value": "authorizationRuleName",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the primary and secondary connection strings for the Namespace"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ef23ca38-0a3b-4999-81d6-8eda310ba63a"
            }
          ]
        }
      ]
    }
  ]
}