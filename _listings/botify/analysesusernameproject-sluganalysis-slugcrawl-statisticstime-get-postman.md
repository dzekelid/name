{
  "info": {
    "name": "Botify Get Analyses Username Project Slug Analysis Slug Crawl Statistics Time",
    "_postman_id": "34c6147d-412f-4008-a8bd-74108511cb42",
    "description": "Return crawl statistics grouped by time frequency (1 min, 5 mins or 60 min) for an analysis",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analyses",
      "item": [
        {
          "id": "714a32fb-9184-490e-b861-26203a49b461",
          "name": "getAnalysesUsernameProjectSlugAnalysisSlugCrawlStatisticsTime",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.botify.com",
              "path": [
                "v1",
                "analyses/:username/:project_slug/:analysis_slug/crawl_statistics/time"
              ],
              "query": [
                {
                  "key": "frequency",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
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
            "description": "Return crawl statistics grouped by time frequency (1 min, 5 mins or 60 min) for an analysis"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "389adda0-d710-40b7-949c-5342cdd8dc00"
            }
          ]
        }
      ]
    }
  ]
}