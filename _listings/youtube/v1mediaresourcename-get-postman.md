{
  "info": {
    "name": "Youtube Get Media Resource Name",
    "_postman_id": "1e5edee6-e830-4d63-b27d-9030e1d1647e",
    "description": "Method for media download. Download is supported\non the URI `/v1/media/{+name}?alt=media`.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "v1",
      "item": [
        {
          "id": "334707c0-756c-4b62-b1a4-b14a7d14e3c2",
          "name": "getV1MediaResourcename",
          "request": {
            "url": {
              "protocol": "http",
              "host": "www.googleapis.com",
              "path": [
                "youtube",
                "v1",
                "v1/media/:resourceName"
              ],
              "variable": [
                {
                  "id": "resourceName",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Method for media download"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f1cb8728-23b3-4706-b669-9831fbfd6314"
            }
          ]
        }
      ]
    }
  ]
}