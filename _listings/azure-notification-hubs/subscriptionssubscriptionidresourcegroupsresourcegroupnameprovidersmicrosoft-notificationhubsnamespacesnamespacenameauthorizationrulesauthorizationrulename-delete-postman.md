{
  "info": {
    "name": "Azure Notification Hubs API Namespaces Delete Authorization Rule",
    "_postman_id": "15f4436a-02d9-4a63-9b71-d6f3bd51aa5e",
    "description": "Deletes a namespace authorization rule",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces authorization rule",
      "item": [
        {
          "id": "c5dab3b7-80cd-4026-b8dd-c5c08fbedacb",
          "name": "Namespaces_DeleteAuthorizationRule",
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
              "id": "3e912690-5dc7-4743-8603-fe6fa692919e"
            }
          ]
        }
      ]
    }
  ]
}