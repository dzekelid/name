{
  "info": {
    "name": "Botify Get Analyses Username Project Slug Analysis Slug",
    "_postman_id": "7c5c2c20-9094-448c-b5ff-3f470d120fc6",
    "description": "Get analyses username project slug analysis slug.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analyses",
      "item": [
        {
          "id": "fc9c5011-f7ad-4ffc-ace5-b5c8026ae04a",
          "name": "getAnalysesUsernameProjectSlugAnalysisSlug",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.botify.com",
              "path": [
                "v1",
                "analyses/:username/:project_slug/:analysis_slug"
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
                },
                {
                  "id": "analysis_slug",
                  "value": "analysis_slug",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get analyses username project slug analysis slug."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "31d354b2-ec58-40ec-a00a-d1a07fdc01b5"
            }
          ]
        }
      ]
    }
  ]
}