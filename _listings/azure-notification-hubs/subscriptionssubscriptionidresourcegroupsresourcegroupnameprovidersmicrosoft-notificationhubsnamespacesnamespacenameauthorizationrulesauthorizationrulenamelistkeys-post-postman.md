{
  "info": {
    "name": "Azure Notification Hubs API Namespaces List Keys",
    "_postman_id": "3cd99ef7-5622-483a-85d6-e372f2f783c6",
    "description": "Gets the Primary and Secondary ConnectionStrings to the namespace",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces keys",
      "item": [
        {
          "id": "f0a51d81-f1fc-498f-90be-a40d786329c7",
          "name": "Namespaces_ListKeys",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.NotificationHubs/namespaces/:namespaceName/AuthorizationRules/:authorizationRuleName/listKeys"
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
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the Primary and Secondary ConnectionStrings to the namespace "
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5d1c0c7e-6637-4f2f-8f3d-186af80f83f3"
            }
          ]
        }
      ]
    }
  ]
}