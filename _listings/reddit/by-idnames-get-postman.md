{
  "info": {
    "name": "Reddit Get By Names",
    "_postman_id": "7c038637-a9fe-4669-a83e-ba81aae29995",
    "description": "Get a listing of links by fullname.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Best",
      "item": [
        {
          "id": "cc6d6498-ac37-46db-98b4-747f9711a654",
          "name": "get&nbsp;Best",
          "request": {
            "url": "http://www.reddit.com/best.json?after=after&before=before&count=count&limit=limit&show=show&sr_detail=sr_detail",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This endpoint is a listing."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "25f17d3e-ddf1-45fb-bcbc-e4ac9319c13c"
            }
          ]
        }
      ]
    },
    {
      "name": "Names",
      "item": [
        {
          "id": "7916d104-1b64-4397-bcd0-590becca2324",
          "name": "get&nbsp;ByNames",
          "request": {
            "url": "http://www.reddit.com/by_id/names?names=names",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a listing of links by fullname."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9692ec4c-e242-45e5-8a59-49d27c067347"
            }
          ]
        }
      ]
    }
  ]
}