{
  "info": {
    "name": "Bitbucket Get Users Username Hooks U",
    "_postman_id": "19268fec-cb4b-4b60-b679-07c4e6ca5e62",
    "description": "Returns the webhook with the specified id installed on the given\nuser account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "67995a4b-7906-4197-b837-39fdab5a8cb6",
          "name": "getUsersUsernameHooksU",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "users/:username/hooks/:uid"
              ],
              "variable": [
                {
                  "id": "uid",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "username",
                  "value": "username",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the webhook with the specified id installed on the given\nuser account"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8e2e4573-85c6-48a5-adc9-303070e8bf2a"
            }
          ]
        }
      ]
    }
  ]
}