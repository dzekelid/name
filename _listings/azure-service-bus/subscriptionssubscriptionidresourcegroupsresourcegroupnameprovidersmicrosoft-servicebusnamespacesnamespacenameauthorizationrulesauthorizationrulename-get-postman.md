{
  "info": {
    "name": "Azure Service Bus API Namespaces Get Authorization Rule",
    "_postman_id": "04c5c856-4fc6-466d-9630-3ea340d2ac1f",
    "description": "Gets an authorization rule for a namespace by rule name.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces authorization rule",
      "item": [
        {
          "id": "e26112b3-7031-4ed0-8cb3-95f5b46bf995",
          "name": "Namespaces_GetAuthorizationRule",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ServiceBus/namespaces/:namespaceName/AuthorizationRules/:authorizationRuleName"
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets an authorization rule for a namespace by rule name"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "14e9109f-37ad-490b-a654-551824824aa3"
            }
          ]
        }
      ]
    }
  ]
}