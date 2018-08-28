{
  "info": {
    "name": "Azure Service Bus API Namespaces Delete Authorization Rule",
    "_postman_id": "6896bdf4-bf35-4885-9feb-158dd8b77840",
    "description": "Deletes a namespace authorization rule.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces authorization rule",
      "item": [
        {
          "id": "de42298b-b569-4e50-b4fd-1e3b7897196f",
          "name": "Namespaces_DeleteAuthorizationRule",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a namespace authorization rule"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e7d2be7b-ed9b-464d-9496-5b9e5a716706"
            }
          ]
        }
      ]
    }
  ]
}