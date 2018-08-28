{
  "info": {
    "name": "Azure Service Bus API Namespaces Delete",
    "_postman_id": "e5d6b8f9-e5c7-43d4-9dec-6b576d5a828b",
    "description": "Deletes an existing namespace. This operation also removes all associated resources under the namespace.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces",
      "item": [
        {
          "id": "5406fd8a-8052-4d2b-b402-ea6d0a3d243c",
          "name": "Namespaces_Delete",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ServiceBus/namespaces/:namespaceName"
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an existing namespace"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d0d75609-1b14-49f4-acf0-2983c6ac955b"
            }
          ]
        }
      ]
    }
  ]
}