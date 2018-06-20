{
  "info": {
    "name": "Botify Get Analyses Username Project Slug Analysis Slug Crawl Statistics",
    "_postman_id": "2e3e3dcd-c96b-4bc8-b257-2ce279548d1c",
    "description": "Get analyses username project slug analysis slug crawl statistics.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analyses",
      "item": [
        {
          "id": "301f1795-512a-4f10-aae5-20cda70b225f",
          "name": "getAnalysesUsernameProjectSlugAnalysisSlugCrawlStatistics",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.botify.com",
              "path": [
                "v1",
                "analyses/:username/:project_slug/:analysis_slug/crawl_statistics"
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
            "description": "Get analyses username project slug analysis slug crawl statistics."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "da350ca9-a34b-49b7-920e-640d2e25cc8c"
            }
          ]
        }
      ]
    }
  ]
}