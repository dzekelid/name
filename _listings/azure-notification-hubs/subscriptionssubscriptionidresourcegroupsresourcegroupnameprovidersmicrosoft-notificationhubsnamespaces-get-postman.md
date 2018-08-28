{
  "info": {
    "name": "Azure Notification Hubs API Namespaces List",
    "_postman_id": "fd086f7a-85d1-4a7d-98ed-81886c8b8ddb",
    "description": "Lists the available namespaces within a resourceGroup.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces",
      "item": [
        {
          "id": "1dc3326c-0d58-4dec-9f50-0f37e9503559",
          "name": "Namespaces_List",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.NotificationHubs/namespaces"
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
            "description": "Lists the available namespaces within a resourceGroup"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e46c0d5d-c138-439f-882f-025322d048ea"
            }
          ]
        }
      ]
    }
  ]
}