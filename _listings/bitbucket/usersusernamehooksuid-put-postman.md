{
  "info": {
    "name": "Bitbucket Update Users Username Hooks U",
    "_postman_id": "aba8a632-72c4-4819-a844-865631e08130",
    "description": "Updates the specified webhook subscription.\n\nThe following properties can be mutated:\n\n* `description`\n* `url`\n* `active`\n* `events`",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "682247b0-5bd6-439b-bed6-e5b87293ce99",
          "name": "putUsersUsernameHooksU",
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
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Updates the specified webhook subscription"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e3f92c6c-9479-4e33-a237-500cf76045fc"
            }
          ]
        }
      ]
    }
  ]
}