{
  "info": {
    "name": "Botify Get Analyses Username Project Slug Analysis Slug Crawl Statistics Urls List Type",
    "_postman_id": "949a9293-62d0-4d59-98c4-413876f8f4ef",
    "description": "Return a list of 1000 latest URLs crawled (all crawled URLs or only URLS with HTTP errors)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Analyses",
      "item": [
        {
          "id": "5e74e54a-cbfc-4e11-b908-030aa470f949",
          "name": "getAnalysesUsernameProjectSlugAnalysisSlugCrawlStatisticsUrlsListType",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.botify.com",
              "path": [
                "v1",
                "analyses/:username/:project_slug/:analysis_slug/crawl_statistics/urls/:list_type"
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
                },
                {
                  "id": "list_type",
                  "value": "list_type",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Return a list of 1000 latest URLs crawled (all crawled URLs or only URLS with HTTP errors)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "38ebad3d-5146-40bb-b625-5444a877a10b"
            }
          ]
        }
      ]
    }
  ]
}