{
  "info": {
    "name": "Healthcare.gov Get Question Page Name Media Type Extension",
    "_postman_id": "ab90cd34-5861-48c7-a8d8-69be8660fa44",
    "description": "Returns pages content.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "insurance",
      "item": [
        {
          "id": "f6e4a141-33cb-42c7-a1f7-61ae65e39d97",
          "name": "returns-pages-content",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.healthcare.gov",
              "path": [
                "question/:pageName:mediaTypeExtension"
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
              "id": "d75afc3f-7a49-4ba3-b50e-7fa5015bfea7"
            }
          ]
        }
      ]
    }
  ]
}