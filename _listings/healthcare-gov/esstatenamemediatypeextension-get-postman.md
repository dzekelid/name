{
  "info": {
    "name": "Healthcare.gov Get State Name Media Type Extension",
    "_postman_id": "022d0e52-f46c-415c-be5d-bb96e8b8d36f",
    "description": "Returns pages content.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "insurance",
      "item": [
        {
          "id": "36aa8365-d255-468c-a358-e0a4f25c1e39",
          "name": "returns-pages-content",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.healthcare.gov",
              "path": [
                "es/:stateName:mediaTypeExtension/"
              ],
              "variable": [
                {
                  "id": "mediaTypeExtension",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "stateName",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns pages content"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "24df805a-63ff-485d-a034-dedd6413ef63"
            }
          ]
        }
      ]
    }
  ]
}