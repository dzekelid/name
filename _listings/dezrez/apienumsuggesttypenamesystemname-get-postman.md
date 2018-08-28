{
  "info": {
    "name": "Dezrez Get enum suggestions for value",
    "_postman_id": "7e3c45cf-19fc-4e98-b922-df3eac499c07",
    "description": "Get enum suggestions for value.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Enum",
      "item": [
        {
          "id": "06e8a1ff-3d6a-4c5e-8080-7d5965805392",
          "name": "Enum_SuggestBytypeNameBysystemName",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dezrez.com",
              "path": [
                "api/enum/suggest/:typeName/:systemName"
              ],
              "variable": [
                {
                  "id": "systemName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "typeName",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get enum suggestions for value."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cc3d8d84-cd0e-4b18-bf78-283bca12b098"
            }
          ]
        }
      ]
    },
    {
      "name": "Feature",
      "item": [
        {
          "id": "b472dc06-d247-4ef8-8877-2802c3e07b2c",
          "name": "Feature_SuggestByname",
          "request": {
            "url": "http://api.dezrez.com/api/feature/suggest?name=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get feature suggestions for value."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2da4c752-5284-4600-86bd-766a2789ec50"
            }
          ]
        }
      ]
    },
    {
      "name": "Tag",
      "item": [
        {
          "id": "68bb58b7-2d52-4d66-845f-83c87ad28f38",
          "name": "Tag_SuggestByname",
          "request": {
            "url": "http://api.dezrez.com/api/tag/suggest?name=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get tag suggestions for value."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8f8a7db5-565f-4170-8c0b-cbb77339f093"
            }
          ]
        }
      ]
    }
  ]
}