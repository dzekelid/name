{
  "info": {
    "name": "Healthcare.gov Get Glossary Page Name Media Type Extension",
    "_postman_id": "ae06b6bf-0f41-461e-b31c-aea42e865f07",
    "description": "Returns pages content.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "insurance",
      "item": [
        {
          "id": "ef6a6036-9a3e-4c8c-ae25-3aecf5d2439f",
          "name": "returns-pages-content",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.healthcare.gov",
              "path": [
                "es/glossary/:pageName:mediaTypeExtension"
              ],
              "variable": [
                {
                  "id": "mediaTypeExtension",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "pageName",
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
              "id": "0b1906eb-281a-4305-a38f-5af08a44afe4"
            }
          ]
        }
      ]
    }
  ]
}