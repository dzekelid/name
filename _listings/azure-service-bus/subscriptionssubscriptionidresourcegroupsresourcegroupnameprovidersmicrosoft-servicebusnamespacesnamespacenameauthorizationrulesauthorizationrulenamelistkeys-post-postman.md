{
  "info": {
    "name": "Azure Service Bus API Namespaces List Keys",
    "_postman_id": "47155ea9-fc24-45ce-8439-9fd1cde41658",
    "description": "Gets the primary and secondary connection strings for the namespace.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces keys",
      "item": [
        {
          "id": "c7c20bdd-6e9e-4f4e-a666-9d8792711af5",
          "name": "Namespaces_ListKeys",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ServiceBus/namespaces/:namespaceName/AuthorizationRules/:authorizationRuleName/listKeys"
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
            "description": "Gets the primary and secondary connection strings for the namespace"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "90974444-1ca7-4199-898f-e961d6792436"
            }
          ]
        }
      ]
    }
  ]
}