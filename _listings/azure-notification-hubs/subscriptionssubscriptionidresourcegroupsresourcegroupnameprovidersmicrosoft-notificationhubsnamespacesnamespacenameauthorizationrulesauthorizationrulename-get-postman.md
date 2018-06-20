{
  "info": {
    "name": "Azure Notification Hubs API Namespaces Get Authorization Rule",
    "_postman_id": "f225ee46-d553-4ec4-b3ad-2a6c1dd7057e",
    "description": "Gets an authorization rule for a namespace by name.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces authorization rule",
      "item": [
        {
          "id": "0837e002-81e0-4f46-baec-8b7efed28c78",
          "name": "Namespaces_GetAuthorizationRule",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.NotificationHubs/namespaces/:namespaceName/AuthorizationRules/:authorizationRuleName"
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
                  "id": "authorizationRuleName",
                  "value": "{}",
                  "type": "string"
                },
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
            "description": "Gets an authorization rule for a namespace by name"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de58abb7-dbbe-4ba1-807f-2e08a322c450"
            }
          ]
        }
      ]
    }
  ]
}