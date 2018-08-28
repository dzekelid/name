{
  "info": {
    "name": "Healthcare.gov Get Glossary Page Name Media Type Extension",
    "_postman_id": "47144d93-ad31-44c6-b7e2-23945d852d78",
    "description": "Returns pages content.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "insurance",
      "item": [
        {
          "id": "0d089f2d-ac35-479d-84e5-d93b0f99d2ca",
          "name": "returns-pages-content",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.healthcare.gov",
              "path": [
                "glossary/:pageName:mediaTypeExtension"
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
              "id": "0fb77e03-ac4c-491d-9bed-b16fa66634d5"
            }
          ]
        }
      ]
    }
  ]
}