{
  "info": {
    "name": "Botify Get Analyses Username Project Slug",
    "_postman_id": "a01ce3c6-d08d-4cdd-a72d-b42974193f55",
    "description": "Get analyses username project slug.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analyses",
      "item": [
        {
          "id": "0f03783f-882a-418a-8aac-ec72a2c38f4f",
          "name": "getAnalysesUsernameProjectSlug",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.botify.com",
              "path": [
                "v1",
                "analyses/:username/:project_slug"
              ],
              "query": [
                {
                  "key": "only_success",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "size",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "username",
                  "value": "username",
                  "type": "string"
                },
                {
                  "id": "project_slug",
                  "value": "project_slug",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get analyses username project slug."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9c476a09-9d0c-40a3-a2d6-82f69d9df1d5"
            }
          ]
        }
      ]
    }
  ]
}