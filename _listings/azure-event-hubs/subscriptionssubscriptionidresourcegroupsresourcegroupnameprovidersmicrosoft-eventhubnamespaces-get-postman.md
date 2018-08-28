{
  "info": {
    "name": "Azure Event Hubs API Namespaces List By Resource Group",
    "_postman_id": "92358919-5a30-40ff-ab2f-989ce9780da8",
    "description": "Lists the available Namespaces within a resource group.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "namespaces resource group",
      "item": [
        {
          "id": "bd85b827-7a5e-4f53-9487-fc336971a4c0",
          "name": "Namespaces_ListByResourceGroup",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.EventHub/namespaces"
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
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the available Namespaces within a resource group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0c76e61-ee49-4c8e-abbf-9cb79d86dd7a"
            }
          ]
        }
      ]
    }
  ]
}