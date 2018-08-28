{
  "info": {
    "name": "Healthcare.gov Get State Name Media Type Extension",
    "_postman_id": "ad468253-cae7-4c9d-a78e-dd76ffbed8c4",
    "description": "Returns pages content.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "insurance",
      "item": [
        {
          "id": "d13646b6-dc53-4f6b-b249-aeb48af6b3d2",
          "name": "returns-pages-content",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.healthcare.gov",
              "path": [
                ":stateName:mediaTypeExtension/"
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
              "id": "4949388f-ba68-4f79-aae2-3790d7c242ca"
            }
          ]
        }
      ]
    }
  ]
}