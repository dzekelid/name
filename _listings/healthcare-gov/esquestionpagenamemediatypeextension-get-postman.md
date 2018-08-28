{
  "info": {
    "name": "Healthcare.gov Get Question Page Name Media Type Extension",
    "_postman_id": "5314e071-a1ed-4673-8083-e1bcdb936d28",
    "description": "Returns pages content.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "insurance",
      "item": [
        {
          "id": "808e41b8-092c-480b-9845-a603980a8cae",
          "name": "returns-pages-content",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.healthcare.gov",
              "path": [
                "es/question/:pageName:mediaTypeExtension"
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
              "id": "e4b975d6-ffd8-4a0e-8786-fb2e8ef3c896"
            }
          ]
        }
      ]
    }
  ]
}