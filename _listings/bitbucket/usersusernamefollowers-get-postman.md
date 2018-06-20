{
  "info": {
    "name": "Bitbucket Get Users Username Followers",
    "_postman_id": "b3792fa5-9024-439e-b866-e93b61928383",
    "description": "Returns the list of accounts that are following this team.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "2e9d8789-e7d2-4262-b463-e5bc244e2acd",
          "name": "getUsersUsernameFollowers",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "users/:username/followers"
              ],
              "variable": [
                {
                  "id": "username",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the list of accounts that are following this team"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "108b5af5-7e0d-4906-a21d-27487030c2ac"
            }
          ]
        }
      ]
    }
  ]
}