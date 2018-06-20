{
  "info": {
    "name": "Azure Notification Hubs API Namespaces List All",
    "_postman_id": "0b24bd54-a208-4503-939c-226697bf3f25",
    "description": "Lists all the available namespaces within the subscription irrespective of the resourceGroups.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces all",
      "item": [
        {
          "id": "17d1ecc7-588b-465f-b459-0cdb7c7e0730",
          "name": "Namespaces_ListAll",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.NotificationHubs/namespaces"
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
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all the available namespaces within the subscription irrespective of the resourceGroups"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ffdd93b1-eac4-4b1f-986a-0c4f8d27b805"
            }
          ]
        }
      ]
    }
  ]
}