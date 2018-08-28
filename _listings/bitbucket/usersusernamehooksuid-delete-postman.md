{
  "info": {
    "name": "Bitbucket Delete Users Username Hooks U",
    "_postman_id": "3069d918-1335-40d1-be72-7d89fcdce866",
    "description": "Deletes the specified webhook subscription from the given user\naccount.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "0c660389-431a-488b-a4d0-7a6936c93516",
          "name": "deleteUsersUsernameHooksU",
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes the specified webhook subscription from the given user\naccount"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2eb44c92-0b19-439a-bf70-123d4d79933d"
            }
          ]
        }
      ]
    }
  ]
}